---
tags: ['2020/[02] February']
title: '6 Feb, Thursday'
created: '2020-02-05T23:45:07.791Z'
modified: '2020-03-19T07:01:17.894Z'
---

# 6 Feb, Thursday

`Day 68`
`Day 8 Aceh`

next: laboratorium langsung
1. tanggal dan jenis kelamin belum dikirim (done)
2. ada bug ketika modal pertama, cek list item laboratoriumnya. duplikat item
3. order item baru gagal: url method not found (done), selanjutnya query error (done)
4. setelah entri item, kan muncul itemnya. itu belum di tambahkan langsung tanggal dan jenis kelamin. 

5. masalah list di laboratorium langsung. entri di pendaftaran langsung tidak masuk ke database (dc_laboratorium) (done: harus di konfirmasi)

6. setelah konfirmasi, ketika aku melihat kembali list (bug dua), darah lengkap muncul dua. lalu kemudian aku hapus, aku tambahkan lagi itemnya, aku konfirmasi, cek muncul tiga. dst
sepertinya ada di `api/pelayanan pemeriksaan_laboratorium_detail`. apakah waktu konfirmasi? disini kekurangan perusahaan adalah tidak menyediakan flowchart. jika menggunakan algoritma yang ada di dinda, muncul satu saja. (found problem) yang jadi masalah adalah relasi ke dc_order_laboratorium. pertanyaannya, ketika list item dihapus, apakah dia juga hapus dari dc_order_laboratorium? query untuk mengambil data item lab ada di `api/pelayanan get_pemeriksaan_laboratorium` (**done: order by ord.id limit 1**)

7. jika di order by, maka yang tampil hanya satu, bukan dua (darah rutin/lengkap), memang tak seharusnya di order by - yang harus kita lakukana adalah menghadapi multiple rows di `dc_order_laboratorium`. solusinya adalah membangun query untuk memfilter hal tersebut. (**done: relasi dc_order_laboratorium menggunakan key yang salah, awalnya menggunakan id_layanan_pendaftaran di tabel dc_layanan_pendaftaran**)

8. lab langsung hasil done, tinggal set tanggal setelah entri. namun setelah dipikir kembali, kita harus mengkonfirmasi lab (perlukah lab langsung dikonfirmasi?) untuk bisa menampilkan item lab yang diuji (**partially done**)

9. Entri lab, (**done**)


rincian transaksi : hapus item, m_pelayanan/delete_pemeriksaan_laboratorium_detail. delete dc_detail_laboratorium, bukan dc_order_laboratorium


## Log
`06.32` datang
