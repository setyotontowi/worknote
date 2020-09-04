---
tags: ['2020/[04] April']
title: 'Apr 20, Monday'
created: '2020-04-19T23:31:15.046Z'
modified: '2020-04-20T22:43:53.948Z'
---

# Apr 20, Monday

`Day 117`

- [X] Setup FG-API-Dinda
- [ ] SIMRS V2: Bobotsari: Update database testing
- [ ] SIMRS V2: Perbaikan tampilan cetak hasil lab [web](https://trello.com/c/6xMhjPmf/83-perbaikan-tampilan-cetak-hasil-laboratorium)
- [ ] Pendaftaran Online Dinda: Registrasi Baru

## Task 1
import database fg_dinda ke postgres
start dumping 09.58
finish 11.08

how to restore a postgres database. 
psql dbname < dump file
jalan. test api.

## Task 2
somehow, unable to connect

## Task 3
Registrasi Pasien Baru

get all data from bundles
confirm dialog
daftar

Pendidikan. lewati dulu

- [x] Masalah alamat
- [x] Bundles
- [ ] Kirim

Task 3.1
Ubah provinsi, kabupaten, kecamatan, 
mau ga mau harus pakai adapter

issues
1. PasienBaru2: Alamat 4: ketika dia di set dari bundle, algoritma filter tidak jalan
2. pendidikan di PasienBaru2 belum ada API nya
3. nama aplikasinya masih temanggung
4. PasienBaru2: Alamat 4: Disable semuanya sebelum form sebelumnya terisi



## Logs
`06.31` start
`08.00` setup FG-API-Dinda
`11.00` selesai setup
`12.23` break; sampai ke masalah alamat, belum selesai.
`22.23` alamat done
`23.42` bundle Pasien3 belum.


