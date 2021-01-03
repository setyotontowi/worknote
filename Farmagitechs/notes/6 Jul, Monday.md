---
tags: ['2020/[07] July']
title: '6 Jul, Monday'
created: '2020-07-06T00:20:10.662Z'
modified: '2020-07-07T02:17:31.153Z'
---

# 6 Jul, Monday

`Day 174` Pendaftaran Online

- Pendaftaran Online: Persiapan Release
- [x] 1. Pendaftaran Online: Pilihan wilayah dibuat dropdown
- [x] 2. Pendaftaran Online: Validasi wilayah
- [x] 3. Pendaftaran Online: Pilihan wilayah tampilan
- [x] 4. Pendaftaran Online: Bug: ketika difilter dan item diclick, maka indeksnya tidak sesuai.
- [x] 5. Pendaftaran Online: Bug: send data to next Pasien3/Pasien1
- [x] 6. Pendaftaran Online: Cek kembali validasi wilayah ketika provinsi diganti. 

## Task 1
- dibuat modal seperti e-doc tampil tipe dokumen. 
  ada method onClick with dialog interface. (stuck)
- atau dengan menambahkan listview dan ketika di click dia akan mengubah button/spinner/dsb ke teks terpilih. memilih item postion yang mengandung object provinsi/kabupaten dsb. `09.03` dialog untuk wilayah sudah tersedia. (complete)
- provinsi dan kota (complete) `09.42`
- kecamatan dan kabupaten (complete) `09.53`

## Task 2
- button kab, kec, kelurahan di disable sebelum provinsi dipilih (complete `09.59`)
- jika provinsi diganti, ke bawahnya juga di kosongkan terlebih dahulu. buat constructor null. set wilayah terpilih sebagai null. provinsi dipilih, maka kabupaten akan terbuka. using method changedstate. but I believe there's another good method. **research nanti**


## Task 3
- ngerapihin code
- tambah button dropdown kecil di kanan button.

## Task 4
- copy all from edoc PasienAdapter

## Task 5
https://stackoverflow.com/questions/39599213

## Task 6
- termasuk bagian research nanti di task 2 note 2. tampaknya bisa menggunakan registerDataSetObserver

## Logs
`07.03` init
`08.00` S1f: Task 1: Try Dialog
`09.14` S2f: Task 1: Dialog muncul dan sudah bisa terfilter
`09.44` S3f: Task 1: untuk Kota
`10.14` S4f: Task 1: complete. Task 2: disabled button
`10.49` S5f: Task 2: Note 2
`13.46` Task 6 complete
`14.01` Task 3, 5 complete


