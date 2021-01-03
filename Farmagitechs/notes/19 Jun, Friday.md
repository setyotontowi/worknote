---
tags: ['2020/[06] June']
title: '19 Jun, Friday'
created: '2020-06-19T01:24:52.637Z'
modified: '2020-06-26T14:03:24.230Z'
---

# 19 Jun, Friday

`Day 163` I can be whoever I want

- [x] SIMRS V2: Hasil Lab pdf tidak keluar di Testing, padahal di lokal keluar: Parent -> 18 Jun
- [x] E-Doc: Revisi 3.1: Problem 2: Revisi: Parent -> 18 Jun
- [x] E-Doc: Side Quest: Redesign: Calendar Pager
- [x] E-Doc: Side Quest: Redesign: Calendar Pager: Filter Calendar
- [x] E-Doc: Revisi 3.2: Search Name wdNy7AXv
- [x] E-Doc: Side Quest: Redesign: Calendar Pager: Bertrubukan dengan Filter Fragment

## Task 1
**Problem**
- khusus print dan ekspor, hasil lab tidak keluar. namun dalam sistem berjalan dengan baik termasuk dengan normal dan abnormalnya. di lokal juga tidak ada masalah yang terjadi.
- menggunakan mas joko juga tidak lengkap databasenya. 

**Hipotesis**
- ada kesalahan di database (tapi hanya print yang tidak bisa)

**Todo**
- cek api printing? tidak melakukan perubahan data apapun.

**Temp**
- `08.57` sedang di test zai. di Live printnya muncul. 

**Finished**
- see temp

## Task 2
**Initial**
tidak dijelaskan permasalahan/pekerjaan apa yang ada di sini. kemungkinan itu terkait dengan dokter yang disimpan menggunakan tombol simpan yang ada di fragment, bukan di dialog

**Problem**
Simpan di SharedPreferences
yang disimpan adalah id dan nama dokternya.
(Revisi, seharusnya ada di button simpan)

## Task 3
**Initial**
- move to this https://github.com/Mulham-Raee/Horizontal-Calendar

**Todo**
- Filter Calendar.


## Task 5
**Problems**
di construct JSON nya, tanggal yang di cari adalah tanggal sekarang. seharusnya mengikuti tanggal di shared preferences atau filtered date nya. 

## Logs

`07.20` init
`08.28` Session 1: Task 1: Gathering information (fin)
`08.58` Session 2: Task 3: Learn and Clone
`09.28` Session 3: Task 3: First Stage Coding on E-Doc
`10.02` Session 4: Task 3: Second Stage Coding (fin)
`10.35` Session 5: Task 4: Revisi
`11.05` Session 6: Task 4: Revisi
`11.37` Interlude
`13.00` Long Session: Redesign Layout.

## Current Status

mengenai edoc. aku mengerjakan secara bersamaan revisi dari mas joko sekaligus redesign. saat ini, aku baru saja menyelesaikan calendar pager di main fragment. namun itu masih belum bisa memfilter tanggal (lebih tepatnya error) dan calendar pager bertrubukan dengan filter fragment. 
