---
tags: ['2020/[06] June']
title: '4 Jun, Thursday'
created: '2020-06-03T23:46:53.404Z'
modified: '2020-06-05T00:54:41.674Z'
---

# 4 Jun, Thursday

`Day 152` Thruster

- [x] SIMRS Report: Perbaikan export excel di menu morbiditas: Setup eLeMoHyL
- [x] SIMRS Report: Perbaikan export excel di menu morbiditas eLeMoHyL
- [x] SIMRS Report: Filter tidak jalan: parent -> task 2
- [x] SIMRS Report: Deploy ke semua rumah sakit versi 2: parent -> task 2
- [x] SIMRS V2: n2AoTkX2, 7S6MTz08, IaWflCWJ
- [x] SIMRS V2: Logo rumah sakit 7S6MTz08

## Task 1
**Problems**
- terkait dengan database yang salah password
- setup fg-auth dan ng-auth nya. terlebih url dan port FG Report.

## Task 2
**Problems**
- cuma muncul TEST di export

**Todo**
- cari route untuk print. 
  - mungkin ada di fg-printing. fg-printing-v2/fg-printingv2/simrs/medical_record/morbiditas/export

**Hypothesis**
- type = "print" di fg_printing/ simrs/medical_record/morbiditas.

**Finished**
- Print/Export terletak di file viewnya, bukan controller. Semua telah aku set berdasarkan metadata. file:pasien_morbiditas.

## Task 3
**Finished**
get_safe(Kelamin), harusnya get_safe(kelamin) di fg_printing

## Task 4
**Todo**
- upload repo (finished)
- update server via ssh
  - PKU Purbalingga 		12.12.12.13    2 (done)
  - Klinik Merden 			12.12.12.15    2 (done)
  - RSGM         				12.12.12.17    2 (done)
  - PKU Merden (Banjar)	12.12.12.14    2 (done)


## Task 5
**Todo**
- n2AoTkX2 upload repo (done)
- 7S6MTz08 upload repo (tidak mengubah apapun) (done)
- IaWflCWJ upload repo (melewati testing) (done)
- update server: [1, 2, 3, 4] (done)

## Task 6
**Problems**
- masih ada data yang tidak sesuai

**Todo**
- pengecekan data di database di setiap RS

## Logs
`06.30` idle
`06.48` start working
`09.40` task 2 finished
`10.59` task 3 finished
`11.28` task 5 finished
