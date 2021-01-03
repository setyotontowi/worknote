---
tags: ['2020/[04] April']
title: 'Apr 21, Tuesday'
created: '2020-04-20T22:15:57.023Z'
modified: '2020-04-21T09:42:58.660Z'
---

# Apr 21, Tuesday

`Day 118`

- [X] Pendaftaran Online Dinda: Registrasi Baru
- [ ] SIMRS V2: Perbaikan tampilan cetak hasil lab [web](https://trello.com/c/6xMhjPmf/83-perbaikan-tampilan-cetak-hasil-laboratorium)
- [ ] SIMRS V2: Rekap Billing: Kolom tindakan tidak muncul (CITO)

## Task 1

- [x] Masalah alamat
- [x] Bundles
- [x] Kirim

Kirim menggunakan dialog '15 menit'
kirim selesai, cuma masih ada yang error di apinya

## Task 2
`sesi 2` start pukul 10.00
Deskripsikan permasalahanannya
kasus ada di rawat inap. keterangan kelas muncul untuk menandakan dia dari kelas mana. tapi requestnya minta dihilangkan saja.
sepertinya itu bermasalah di margin kelas yang diambil

## Task 3
Kasus Lokal Resa Q 00000005 - Tindakan Aff Cateter / DC Rawat Inap
Laporan: Kolom tindakan di pasien rawat inap tidak muncul.
apakah tetap muncul di pelayanan? (muncul)

file yang dibutuhkan
- [FRONT] keuangan/billing/rekap_billing. button mata mengeksekusi detail_billing listener. membuka #detail_modal. dengan mengambil api api/keuangan/rekap_billing_detail/ 
- di file api/keuangan/rekap_billing_detail sini `$val->tindakan = $this->m_keuangan->get_tarif_tindakan_list($val->id, 'Ya');` dia mereturn 

```sql
select tk.*, l.nama as item, l.id as id_layanan,
IFNULL(pj.nama, '') as penjamin,
IFNULL(pj.diskon, '-') as diskon,
tk.total as harga_item, 
sum(tk.total) as total,
sum(tk.total) as tagihan, 
count(*) as frekuensi
from dc_pendaftaran pd 
join dc_layanan_pendaftaran lp on (lp.id_pendaftaran = pd.id)
join dc_tarif_tindakan tk on (tk.id_layanan_pendaftaran = lp.id)
join dc_komponen_tarif kt on (kt.id = tk.id_komponen_tarif)
join dc_layanan l on (kt.id_layanan = l.id) 
left join dc_penjamin pj on (pj.id = tk.id_penjamin)
where lp.id = '7' 

*and tk.pendaftaran = 'Ya'

group by kt.id, DATE_FORMAT(tk.waktu, '%Y-%m-%d %H:%i')
order by tk.id
```

*yang bermasalah

- Quick Solution: and tk.pendaftaran = 'Tidak' which is argumen get_tarif_tindakan_list sebelumnya diubah dari 'Ya' menjadi 'Tidak'. Pengecekan dilakukan dengan membandingkan dengan SIMRS Dinda (Versi 1) dan memang defaultnya adalah 'tidak'


## Logs
`05.16` start
`08.31` task 1 finish
`15.47` task 3 start
`16.42` task 3 finish
