---
tags: ['2020/[07] July']
title: '8 Jul, Wednesday'
created: '2020-07-08T00:13:11.782Z'
modified: '2020-07-10T08:08:49.146Z'
---

# 8 Jul, Wednesday

`Day 176` Stay on the rythm

- [x] Pendaftaran Online: Validasi yang lainnya. 
- [x] Pendaftaran Online: Fitur Tambah KTP
- [x] Pendaftaran Online: Bug, Wilayah dari fragment lainnya (onHold)
- [ ] Pendaftaran Online: Conflict getBundle dan RegisterDataObserver -> task 3
- [x] Pendaftaran Online: Kirim Dokumen

## Task 1
- ada 4 validasi: kelurahan, email, KTP, tanggal lahir, nama (complete)
- untuk alamat, tidak aku beri


## Task 2
- ada di Pasien4 (setelah pasien 3)
- dia terdiri dari header, terus di tengahnya ada kotak untuk nampilin gambar. terus ada button "ambil gambar"

## Task 3
- ketika dari Pasien3 atau Pasien2, ketika mengubah wilayah dia tidak bisa di klik atau ketika dipilih, dia kosong, khususnya kabupaten kebawah. solusinya, ambil dari bundle lalu masukkan ke parameter dengan default null. 
- revisi. ini conflict antara getBundle dengan RegisterDataObserver ketika data berubah. (onHold). Ketika getBundle, dia akan memanggil kembali getWilayah agar dataset tersedia dan bisa diganti. Karena databerubah, maka dia mentrigger RegisterDataObserver dan mengeksekusinya. sehingga button dibawahnya menjadi false atau berubah menjadi "Kabupaten" bukan nama kotanya. akan dikerjakan setelah membuat activity baru Fitur Tambah KTP. kemungkinan inin masih bisa diakali (extend to task 4) (`10.29`)

## Task 4
**Todo List**
- Tambah Activity Baru (`13.10`)
- Ubah action selesai pada Pasien3 menjadi intent (`13.10`)
- kirim datanya (`13.10`)
- Button buka kamera di Activity Baru (`13.25`)

## Task 5
kirim via Form Data


## Logs
`07.01` init
`09.27` task 1 validasi text complete
`09.55` task 1 complete
`10.29` task 3 complete
`13.32` task 4 complete
`13.44` merapikan tampilan PasienBaru4
