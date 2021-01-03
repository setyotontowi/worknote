---
tags: ['2020/[03] March']
title: Weekly Task
created: '2020-03-09T01:03:52.425Z'
modified: '2020-08-07T06:03:37.664Z'
---

# Weekly Task

## Week `11` Mar 9 - 13
- [X] E-Doc: Login, List selesai.
- [ ] RS Abby: installing Kategori nilai normal. 
- [X] Pendaftaran Online Dinda: Configuration.

## Week `12` Mar 16 - 20
- [X] Pendaftaran Online Dinda: Milestone 1 Login RM
- [X] E-Doc: Pdf Library
- [X] E-Doc: FingerPaint
- [X] E-Doc: Revisi 1: List Pasien <mark>see wednesday</mark>

## Week `13` Mar 23 - 27
- [X] E-Doc: Revisi 1: Filter <mark>see week `12`</mark>
- [x] E-Doc: Flatten FingerPaint

## Week `14` Mar 30 - Apr 3
- [x] E-Doc: Revisi 1: List Document <mark>see week `12`</mark>
- [x] Pendaftaran Online Dinda: Milestone 2 Pasien Baru

### Attached Notes
[API Doc Pendaftaran Online Dinda](1)
[API Doc E-Doc](2)

[1]: https://www.dropbox.com/s/thd34988tiqxv8y/DOKUMENTASI%20FG-API-DINDA.doc?dl=0
[2]: https://documenter.getpostman.com/view/3744790/SzYUYfn3?version=latest

### Issues `Pendaftaran Online`
1. logout masih belum bisa, dia menggunakan API. apakah mau diganti dengan menghapus sharedpreferences?
2. Registrasi user masih belum jelas
3. No RM ambil dari shared preferences
4. SharedPreferences login belum diubah

### Issues `E-Doc`
1. ~~CheckToken ke General Helper dengan membuat fungsi berlapis. Callback dibungkus kembali ke fungsi (done)~~
2. Password salah, dia langsung force close.
3. Left Fragment Border
4. ~~Back button masih tidak bisa. onBackPressed? (done)~~
5. Header di set di GeneralHelper
6. ~~Memperbaiki View di List Pasien, beserta classnya.~~
7. ~~CheckToken tidak bisa digunakan ketika aplikasi keluar lalu masuk kembali.~~
8. Toggle Filter touch di luar area.
9. Filter slide menggeser layout lainnya.
10. List Pasien masih belum sesuai
11. Filter Fragment height masih belum sesuai
12. Jika layanan poli maka klinik tampil, jika ranap maka bangsal tampil, jika UGD maka tidak ada yang tampil
13. Filter Fragment, tanggal harus ada maka buat sejenis validasi.
14. ListPasien, setelah di refresh datanya melalui filter dia tidak mereplace namun menumpuk. sementara menggunakan background
15. Poli, Tanggal, sebaiknya masuk sharedpreferences
