---
tags: ['2020/[04] April']
title: Weekly Task
created: '2020-04-01T00:42:14.137Z'
modified: '2020-08-07T06:03:05.717Z'
---

# Weekly Task

## Week `14` Mar 30 - Apr 3
- [x] E-Doc: Revisi 1: List Document <mark>see week `12`</mark>
- [x] Pendaftaran Online Dinda: Milestone 2 Pasien Baru

## Week `15` Apr 6 - Apr 8
- [x] E-Doc: Revisi 1
- [X] Pendaftaran Online Dinda: Milestone 2: Pasien Baru

## Week `16` Apr 13 - Apr 17
- [X] E-Doc: Revisi 1: Pasien
- [x] Pendaftaran Online Dinda: Milestone 2: Pasien Baru
- [X] SIMRS Report Abby: Export rekam medis ranap/rajal: tambah total

## Week `17` Apr 20 - Apr 24
- [x] Pendaftaran Online Dinda: Beta (22)
- [x] SIMRS V2: Rekap Billing: Tindakan di ranap tidak muncul (22)
- [x] SIMRS V2: Hasil Lab: Perbaikan tampilan cetak hasil lab (21-24) (see 24)

## Week `18` Apr 27 - Apr 30
- [x] E-Doc: Pdf Engine (done by mas joko)



### Issues `E-Doc`
1. ~~CheckToken ke General Helper dengan membuat fungsi berlapis. Callback dibungkus kembali ke fungsi (done)~~
2. ~~Password salah, dia langsung force close.~~
3. ~~Left Fragment Border~~
4. ~~Back button masih tidak bisa. onBackPressed? (done)~~
5. ~~Header di set di GeneralHelper~~
6. ~~Memperbaiki View di List Pasien, beserta classnya.~~
7. ~~CheckToken tidak bisa digunakan ketika aplikasi keluar lalu masuk kembali.~~
8. Toggle Filter touch di luar area.
9. ~~Filter slide menggeser layout lainnya.~~ tidak dipilih
10. ~~List Pasien masih belum sesuai~~
11. ~~Filter Fragment height masih belum sesuai~~
12. ~~Jika layanan poli maka klinik tampil, jika ranap maka bangsal tampil, jika UGD maka tidak ada yang tampil~~
13. ~~Filter Fragment, tanggal harus ada maka buat sejenis validasi.~~
14. ~~ListPasien, setelah di refresh datanya melalui filter dia tidak mereplace namun menumpuk. sementara menggunakan background~~
15. Poli, Tanggal, sebaiknya masuk sharedpreferences
16. ~~Filter Fragment, ada perubahan di headerPost, ini yang membuat ada bug baru. `parent 5`~~
17. Pasien kartu masih belum sesuai
18. ~~class Pasien perlu disesuaikan~~
19. check all variables (codeReview) `p18`
20. Pasien list document seharusnya di group per tanggal `p17`
21. List Pasien variables disesuaikan `p.19`
22. Header tanggal di List Pasien
23. UI: mobile phone alternatives.
24. Responsive Filter Pasien

### Deploy `E-Doc`
1. Sesuaikan tanggal list pasien

---

### Random Note #1 on Sunday Apr 12, 21.59
Berarti issues masih terdiri dari Filter Fragment, Pasien Action and Some Others.
Alur yang dibutuhkan untuk membuat document. 
1. /api/document_history/list_doc Ditampilkan di List Doc.
2. /api/document_history/create_doc To Create Document
3. /api/document_history/list_doc To Download PDF


### Setup SIMRS Report

1. setting javac and java to 8
2. run fg-resources in htdocs (FG-Resources)
3. run fg-auth in feb 21 (FG-Auth)
4. Projects/FG-Report/fg-report sbt (FG-Report)

important note
- check simrs_ng
- untuk export, ada di htdocs fg-printing

### SIMRS V2 Issues
1. di Apr 23, tracking masalah kkt.id atau nama. di live, juga dimana ia digunakan. siapa yang membuat hal tersebut.

