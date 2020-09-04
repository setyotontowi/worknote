---
tags: [2019/December]
title: '19 Dec, Thursday'
created: '2019-12-19T00:45:40.037Z'
modified: '2019-12-19T08:51:12.802Z'
---

# 19 Dec, Thursday

`Day 36`

- [ ] 1. SIMRS Dinda : Pembuatan Masterdata baru, (Filtering di Hasil Lab)
- [ ] 2. SIMRS Temanggung : Log Masterdata

## Task 1
Tujuan, filter pasien di hasil lab berdasarkan usia. 
Surepah Ny. jenis kelamin?

jenis kelamin di kategori nilai normal tidak mengikuti enum sehingga lebih dinamis. **keputusanku** adalah tetap menampilkan semua jenis kelamin, sementara yang difilter hanyalah usia.

Analisis 
- di api permintaan_pemeriksaan_laboratorium_get cuma bertujuan untuk meminta data hasil laboratorium. tidak ada data pasien yang didapatkan disana. berarti ketika meminta di view, kita kirimkan tanggal lahir juga.
- sewaktu pembentukan teks, berarti juga diperhitungkan. karena sewaktu filtering di query dia menggunakan item_laboratorium (done)
- algoritma untuk menggenerate teks di kolom nilai_normal : diambil datanya dari semua yang memiliki id_item_lab, dan digenerate ulang. seharusnya satu-satu, tidak digabungkan. lalu bagaimana mengambilnya dari hasil laboratorium.
- jika di dc_nilai_normal diubah menjadi persatu. karena relasinya dari item_lab, maka kategori akan diabaikan. solusinya : tambah satu tabel entah apa agar bisa merelasikan pasien dengan kategori. (where dc_nilai_normal.kategori = id.dc_kategori_nilai_normal and $usia between dc_kategori_nilai_normal.awal and akhir) (done)
- relasi sudah muncul. namun, jika data yang diambil dua, maka akan muncul dua form alih alih satu form dengan nilai normal yang digabungkan. (select concat from (select... query 2)) (done)
- penambahan nilai normal langsung dari hasil lab - berarti, default kategorinya null <- perlu dicek


Query untuk mengambil hasil lab dan nilai normalnya
``` sql 
select a.*, group_concat(a.nilai_normal_lab) as nilai_normal_asli from 
(select idl.*, nl.nilai_normal as nilai_normal_lab,
IFNULL(st.nama, '') as satuan  
from dc_item_detail_laboratorium idl 
left join dc_nilai_normal_lab nl on (idl.id_item_laboratorium = nl.id_item_laboratorium) 
left join dc_satuan st on (st.id = idl.id_satuan) 
left join dc_kategori_nilai_normal knn on (nl.kategori = knn.id)
where idl.id_detail_laboratorium = 112829 and (knn.id = 3 or knn.id = 2)) a
```

- filter usia sudah berhasil, namun filter jenis kelamin malah tidak muncul. mau tidak mau filter jenis kelamin harus dibedakan, mungkin dimasukkan ke enum. dan juga parameter tanggal serta jenis kelamin di views belum dinamis

## Log
`07.24` datang
`08.42` drawing
`09.04` task 1 masterdata done
`09.55` etiket tangerang, sedikit bug.
`10.41` rs temanggung things
`15.03` sampai akhir hayat
`15.51` pulang

