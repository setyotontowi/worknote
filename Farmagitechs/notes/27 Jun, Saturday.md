---
tags: ['2020/[06] June']
title: '27 Jun, Saturday'
created: '2020-06-26T22:55:18.507Z'
modified: '2020-07-04T01:56:13.066Z'
---

# 27 Jun, Saturday

`Day 168` Jaga Sabtu

- [x] E-Doc: Planning
- [x] SIMRS Report: Export Kunjungan Laboratorium dan Kunjungan Radiologi: BX0wVWrG

## Task 1
- Swipe down to refresh
- Header kartu jumlah kunjungan pasien
- Pengecekan satu per satu class dan perapihan code

## Task 2
cd Program/report-v2/reportv2

Rute dari printing
Printing mengambil dari excel di program php. sedang apinya mengambil dari simrs. 
jika melakukan penambahan kolom, maka yang dilakukan adalah mengecek apinya. apakah ada data yang akan ditambahkan atau tidak. kemudian ditampilkan di view php untuk exportnya. tidak melalui scalanya kok.

**Note**
- Sinkronisasi database lokal dengan history sql
- keterangan dokter ada di dc_detail_radiologi, sedangkan query di source code hanya sampai dc_radiologi.
- keterangan dokter bisa jadi ambigu. karena dokter yang bertanggung jawab adalah per item radiologinya, bukan per polikliniknya nya. jadi dokter poliklinik itulah dokter pengirim sedangkan dokter di hasil item radiologinya adalah dokter penanggung jawab. 



## Logs
`05.55` Prework
