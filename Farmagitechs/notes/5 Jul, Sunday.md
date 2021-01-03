---
tags: ['2020/[07] July']
title: '5 Jul, Sunday'
created: '2020-07-05T02:41:25.180Z'
modified: '2020-07-07T13:56:34.136Z'
---

# 5 Jul, Sunday

`Additional`

Selalu buat rencana koding terlebih dahulu

- [x] 1. E-Doc: Create layout for dialog -> 2 Jul, Task 3
- [x] 2. E-Doc: Thumbnailing -> 2 Jul, Task 3
- [x] 3. E-Doc: Thumbnailing per item -> Task 2
- [x] 4. E-Doc: Add Document similar to prior dialog
- [x] 5. E-Doc: Bug, Simpan dokumennya gagal. -> 2 Jul, Task 3
- [ ] 6. E-Doc: Rev, override back button ke main fragment -> 2 Jul, Task 3
- rencana untuk menggunakan model sebagai package apinya
- desain reference for add dialog
- create object Document which extends of TypeDocument and Pasien

## Task 2
- using StringRequest lalu convert hasil [string nya ke bitmap](https://stackoverflow.com/questions/23005948) coba dulu di Bitmapnya. (compl, menggunakan imagerequest)
- masukkan ke Object Tipe Dokumen (compl)
- mAdapterUpdate (compl)

## Task 3
- foreach dokumenlist, get dokumen id terus panggil getThumbnailnya terus sewaktu callback, adapternya diupdate. _problem_ karena asinkronus, tipe dokumen akan kosong terlebih dahulu. (completed)

## Task 4
- Add button (complete)
- Kitchen: Class needed. ada dua method yang dibutuhkan dan semuanya ada di dalam di PasienFragment. bisakah kita migrasi ke TipeDokumenAdapter? dengan mempertimbangkan contextnya (complete)

## Task 5
- lihat di apinya apakah ada tanggalnya? pake reg number (compl)
- debug dengan cara membuat dokumen lagi. kali ini pastikan dua apinya terpanggil tanpa ada yang error (compl, sepertinya errornya ada di Pasien bagian document adapternya, di bagian classnya)
- identify adapter

## Logs
`09.42` start
`10.22` task 2 complete
`10.42` task 3 complete (1 Jam)
`16.18` start
`17.03` task 4 complete
`17.23` finished (1 jam 5 menit)
`19.42` start
`20.36` task 5 complete (54 menit) (Total 3 Jam)
