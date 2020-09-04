---
tags: ['2020/[02] February']
title: '5 Feb, Wednesday'
created: '2020-02-05T03:16:37.761Z'
modified: '2020-03-19T07:01:17.869Z'
---

# 5 Feb, Wednesday

`Day 67`
`Day 7 Aceh`

- [ ] Setting FG Report
- [ ] Deploy SIMRS V2 Nilai normal

yang nilai normal, ada sedikit perubahan. versi mysqlnya beda, kah? cek di repo.

seketika banyak yang error. seperti query di item_laboratorium, tiba-tiba error ketika menggunakan databaseku. apakah akan aku perbaiki atau seperti apa adanya saja?
apa adanya saja. ketahuilah, sebenarnya ada di m_masterdata : line 4935. kt_rujukan sudah ada terlebih dahulu. yang jadi masalah memang kt.rujukannya.

buat skenario testing..
sepertinya data yang ada sekarang adalah data darah.

darah rutin, done.
pasien atas nama najwa shihab
ada error mendeteksi abnormal. tidak tersimpan hingga level databases
print masih ada error..
keseleruhan adalah menu hasil_laboratorium

cek tabel dc_item_detail_laboratorium di simrs_dinda.
hasil_lab printing done.

next: laboratorium langsung
- tanggal dan jenis kelamin belum dikirim (done)
- ada bug ketika modal pertama, cek list item laboratoriumnya. duplikat item
- order item baru gagal: url method not found (done), selanjutnya query error (done)
- setelah entri item, kan muncul itemnya. itu belum di tambahkan langsung tanggal dan jenis kelamin. itu aku jadikan satu aja dengan bug kedua. masalah list di laboratorium langsung.


## Log
`09.20` datang
