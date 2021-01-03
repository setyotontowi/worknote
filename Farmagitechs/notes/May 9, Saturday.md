---
tags: ['2020/[05] May']
title: 'May 9, Saturday'
created: '2020-05-09T01:46:39.757Z'
modified: '2020-05-11T06:06:39.738Z'
---

# May 9, Saturday

`Day 138` It's been for a while since i'm not properly working

- [ ] SIMRS V2: List tindakan dijadikan satu dengan total jumlah di rincian billing: c/ixl5cRbj
- [ ] SIMRS V2: beda tindakan di pelayanan dan di rincian billing: parent->task 1
- [ ] SIMRS Temanggung: Tindakan Operasi di Pembayaran tidak ada: c/4PAX0NJW

prioritaskan task 2

## Task 1

studi kasus: makan banyak ditulis satu demi satu. tindakan banyak juga serupa.
cek di kasus rawat inap. 

```
# ABAIKAN
problem encounter: The MongoDB PECL extension has not been installed or enabled.
two options:
1. installing mongoDB extension
2. disabling mongoDB (the fastest way if anything didn't work)
3. see autoload in ssh

tried 3 but repos encrypted. have an idea using ssh pass but didn't brave enough.
option no 2 how to disabled it? by manual one by one. NOTED

```

ada bug baru di komen trello tersebut. (Task 2)

**Edit**: tindakan yang dijadikan satu adalah yang di cetak (print)

> On Hold
  permasalahannya adalah qty dan frekuensi. jika perhitungan yang digunakan adalah frekuensi, maka qty tidak akan berpengaruh.


## Task 2

Step by step
1. check apakah ini ada sangkut pautnya sama perubahan logdata?
2. cek ke table mana dia masuk, pengecekan dimulai dari pelayanan->rawat inap atau poliklinik

setelah di cek di table dc_tarif_tindakan, datanya telah masuk. id 2463 (makan)
apakah rekap biling mengambil dari dc_tarif_tindakan?

m_keuangan:

``` sql
select tk.*, l.nama as item, l.id as id_layanan,
IFNULL(pj.nama, '') as penjamin,
IFNULL(pj.diskon, '-') as diskon,
tk.total as harga_item, 
sum(tk.total) as total,
sum(tk.total) as tagihan, 
* count(*) as frekuensi

from dc_pendaftaran pd 
join dc_layanan_pendaftaran lp on (lp.id_pendaftaran = pd.id)
join dc_tarif_tindakan tk on (tk.id_layanan_pendaftaran = lp.id)
join dc_komponen_tarif kt on (kt.id = tk.id_komponen_tarif)
join dc_layanan l on (kt.id_layanan = l.id) 
left join dc_penjamin pj on (pj.id = tk.id_penjamin)
where lp.id = '2463' and tk.pendaftaran = "Tidak" group by kt.id, DATE_FORMAT(tk.waktu, '%Y-%m-%d %H:%i')
order by l.nama, waktu

* mispersepsi
```

> Solution
  mispersepsi, yang dihitung adalah frekuensinya, bukan qty nya. Dan yang tampil di view adalah frekuensi. maka ini dianggap selesai.

## Logs
`08.46` start
`13.07` task 1 and task 2 on hold. masalah frekuensi dan qty masih belum clear. 
``
