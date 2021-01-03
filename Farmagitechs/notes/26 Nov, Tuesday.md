---
tags: [2019/November]
title: '26 Nov, Tuesday'
created: '2019-11-26T00:53:31.651Z'
modified: '2019-11-26T08:22:43.328Z'
---

# 26 Nov, Tuesday

`Day 20`

- [ ] SIMRS Documentation
- [X] SIMRS Temanggung : Penyesuaian Label ICD X
- [X] SIMRS Temanggung : Revisi Etiket Bank Darah
- [X] SIMRS Temanggung : Perubahan label di html di pemeriksaan IGD
- [X] SIMRS Temanggung : Penambahan tabel diagnosa di export pemeriksaan IGD

## Task 2

- Penghilangan seperator '|'
- Pelayanan > Pemeriksaan Klinik, Pemeriksaan IGD, Rawat Inap

Dalam Menu:
- [X] Pemeriksaan Klinik
- [X] Pemeriksaan IGD
- [X] Rawat Inap

File yang terlibat
views/pelayanan/pemeriksaan/pemeriksaan_poli.php
views/pelayanan/pemeriksaan/diagnosa_tindakan_form.php ```on line 112```

Turns out they used same file = diagnosa_tindakan_form.php

## Task 3

- tolong ditambah keterangan tgl cetak di pojok kanan atas, font nya lebih kecil ya @setyotontowi .. format >>> tanggal cetak : dd/mm/yyyy

## Task 4

Tulisan label Respon time di ubah menjadi --> respon time IGD
tulisan label respon time bawah di ubah menjadi --> respon time ponek
**files :**
views/pelayanan/pemeriksaan/pemeriksaan_igd.php

## Task 5 

files :
controllers/export export_pemeriksaan_igd()
views/export/pelayanan/list_rawat_jalan.php
models/m_pelayanan.php get_diagnosa()

## Task Bonus

Log Login Bug
1. fungsi untuk memasukkan log dan mengupdatenya (logout) aku salin dari controllers/users ke controllers/app 

## Log
`07.35` datang
`09.05` Task 1, random notes
`09.18` Task 2
`09.50` Routing Selesai
`10.05` Task 2 Done
`10.20` Task 3 Done
`10.38` idle
`10.45` Task 4 Done
`11.07` Revisi minor
`12.23` Task 5 Done
`14.27` Log Login Bug
