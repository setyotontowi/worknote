---
tags: ['2020/[07] July']
title: '2 Jul, Thursday'
created: '2020-07-02T01:20:19.876Z'
modified: '2020-07-05T13:49:21.344Z'
---

# 2 Jul, Thursday

`Day 172` Percaya seutuhnya

Hari ini, baterai laptopku menjumpai issue yang tidak menyenangkan. Plugged in but it's not charging

- [x] 1. E-Doc: Konfigurasi kembali model Pasien.class -> 1 Jul
- [x] 2. E-Doc: List yang dipilih, warnanya menjadi gelap.
- [x] 3. E-Doc: Penambahan Activity tambah document
- [x] 4. E-Doc: Konfigurasi lanjutan model Pasien -> Task 1
- [x] 5. E-Doc: Set Text Tanggal Lahir dan Tanggal Visit -> Task 4
- [x] 6. E-Doc: Floating Action Tambah Document -> Task 3
- [x] 7. E-Doc: Log Data di setiap url API nya

**Note**
- DateFormatter dimasukkan ke general helper

Alur pengerjaan: Dimulai dari task 1 kemudian lanjut ke task 3 karena minggu depan dibutuhkan updatenya.

## Task 1
karena api antara visitasi dan pasien berbeda. jadi tidak bisa dijadikan satu kelas. 

## Task 3
- penambahan dokumen bisa disimpan di sqlite terlebih dahulu
1. Floating Action Button (Task 6)
2. New Activity
3. Construct a layout, including API for getting document image
4. Modal dialog for preview and adding attributes

## Task 4
Mengambil api dari pasien_get. dengan callback seperti checkAuth.

## Task 5
somehow tanggalkunjungan tidak bisa disimpan datanya dari ListPasienFragment
kemungkinan pertama masalah parcelable
`10.44` permasalahannya pasien.getTanggalKunjungan selalu null

**complete**
tanggal kunjungan aku taruh di callback



## Logs
`07.01` start
`08.23` task 1
`08.49` Session 1 Finished: Task 1: Class
`09.19` Session 2 Finished: Task 4: Get from api
`09.49` Session 3 Finished: Task 5: Tanggal kunjungan
`10.19` Session 4 Finished: Task 5: Debugging
`10.49` Session 5 Finished: Task 5: Debugged
`14.26` Task 2 complete
