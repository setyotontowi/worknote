---
tags: ['2020/[05] May']
title: 'May 11, Monday'
created: '2020-05-11T01:05:40.052Z'
modified: '2020-05-11T07:03:26.955Z'
---

# May 11, Monday

`Day 139` This likely will be a busy day

- [x] SIMRS Temanggung: Tindakan Operasi di Pembayaran tidak ada: c/4PAX0NJW: Kalibrasi database (Onhold)
- [x] SIMRS V2: beda tindakan di pelayanan dan di rincian billing: parent: May 9
- [ ] SIMRS V2: Operasi IGD /c/ahE4r6Dy/ (Onhold)
- [ ] SIMRS V2: validate count(*) as frekuensi di beberapa fungsi: parent->2
- [ ] SIMRS V2: List tindakan dijadikan satu dengan total jumlah di rincian billing: c/ixl5cRbj

## Task 1
Problems: database tidak ada
Elbow Grease: approximate time: 3 hours

Untuk kasus ini ada tiga opsi:
1. Menggunakan database mas enggar/online (the quickest)
2. Kalibrasi database (the most complicated)
3. Mengunduh 5GB database temanggung

> Onhold - Override Mas Enggar
  tetap menyiapkan databasenya sekaligus membuat mappingnya. Opsi 2 digunakan. sementara ini tasknya di oper ke mas enggar

## Task 2
**Problems**
Rekap Billing yang digunakan adalah qty, bukan frekuensi

**Files**
m_keuangan:

```sql
select tk.*, l.nama as item, l.id as id_layanan,
IFNULL(pj.nama, '') as penjamin,
IFNULL(pj.diskon, '-') as diskon,
tk.total as harga_item, 
sum(tk.total) as total,
sum(tk.total) as tagihan, 
-- count(*) as frekuensi
++ sum(qty) as frekuensi

from dc_pendaftaran pd 
join dc_layanan_pendaftaran lp on (lp.id_pendaftaran = pd.id)
join dc_tarif_tindakan tk on (tk.id_layanan_pendaftaran = lp.id)
join dc_komponen_tarif kt on (kt.id = tk.id_komponen_tarif)
join dc_layanan l on (kt.id_layanan = l.id) 
left join dc_penjamin pj on (pj.id = tk.id_penjamin)
where lp.id = '2463' and tk.pendaftaran = "Tidak" group by kt.id, DATE_FORMAT(tk.waktu, '%Y-%m-%d %H:%i')
order by l.nama, waktu

```

> Solution
  `count(*) as frekuensi` diganti `sum(qty) as frekuensi`


**Validate**
setelah di cek, ternyata di file yang sama terdapat 8 fungsi yang menggunakan `count(*) as frekuensi`
confirm: diganti

**Function**
- get_tarif_tindakan_list (problem awal: done)
- get_tarif_operasi_list
- get_tarif_hemodialisa_list
- get_tarif_laboratorium_group
- get_tarif_radiologi_group
- get_tarif_fisioterapi_group
- tagihan_tindakan
- tagihan_operasi

**To Do**
cari dimana operasi-operasi tersebut dibuat: further task


## Task 3
**problems**
ada error ketika transaksinya yang terjadi di lokalku.

e: semua database live untuk dc_tarif_operasi memiliki 14 kolom. tapi codingnya memerlukan 19 kolom.
e: semua database live versi 1 dc_tarif_operasi memiliki 26 kolom.

**Problems**
Meskipun struktur database dan repository sama antara live rsgm dan lokal, namun terdapat ketidaksuaian error: di live error nopolish tidak terjadi, di lokalku terjadi. 
**Hipotesis**
Cara input maya dengan aku berbeda.

> Onhold: permasalahan terlalu rumit. perlu analisis lebih lanjut.

## Task 4
**Problems** 
validasi fungsi-fungsi yang menggunakan count(*) as frekuensi. Apakah akan ditemukan kasus serupa dengan qty.


## Logs
`08.06` start
`09.15` task 1 override
`10.30` task 3 onhold
`13.26` start task 2
