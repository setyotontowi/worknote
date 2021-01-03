---
tags: ['2020/[06] June']
title: '22 Jun, Monday'
created: '2020-06-22T01:17:19.710Z'
modified: '2020-06-26T01:50:06.691Z'
---

# 22 Jun, Monday

`Day 164` E-Doc, Cleansing

- [x] E-Doc: Minor Bug #1: Parent -> 19 Jun Task 6
- [x] E-Doc: Minor Bug #2
- [x] E-Doc: Minor Bug #3: Parent -> 19 Jun Task 4
- [x] E-Doc: Minor Bug #4: Parent -> 19 Jun Task 5
- [x] E-Doc: Minor Bug #5

## Task 1
**Todo**
- Cek penempatan layout (done)
- gravity, animation filter fragment diatur

**Decision**
- Redesign Fragment, muncul dari bawah

## Task 2
**Problem**
Calendar pager bertrubukan dengan main fragment

## Task 3
**Problem**
- Calendar Pager filter belum jalan
- setelah calendar pager di set ke tanggal tertentu, volley tidak jalan: kurang pasien

## Task 4
**Problems**
- di construct JSON nya, tanggal yang di cari adalah tanggal sekarang. seharusnya mengikuti tanggal di shared preferences atau filtered date nya. 
- `13.46` problemnya implementasi ke filter fragment: todo #2

**Todo**
- using filter recyclerview https://www.androidhive.info/2017/11/android-recyclerview-with-search-filter-functionality/
- ListPasienFragment dan Adapter di inisiasikan di mainnya.

**Note**
- `14.24` filter terpanggil namun hasilnya selalu 0, proses pemanggilan adapter sepertinya sudah benar  ;

**Finished**
using recylerview implement filterable

## Task 5
**Problem**
Click outer filter fragment to hide or auto hide setelah fragment tampil. ato, add close button

**Todo**
- di outer layer, terdapat layout seluas layar. mungkin bisa dikasih background gelap sedikit transparan ketika itu di klik, maka filter fragment akan di hide.


## Logs
`07.21` Init
`08.38` Session 1: Task 1: Initial
`09.08` Session 2: Task 1: First Stage Coding: Bottom Fragment
`09.38` Session 3: Task 1: Second Stage Coding: fin, rearranging task
`09.59` extra 3 min
`10.08` Session 4: Task 2: fin, Task 3: change bulan to certain date
`10.43` Session 5: Task 3: Second Stage Coding: debuggin calendar
`11.13` Session 6: Task 3: Third Stage Coding, fin
`11.28` extra 10 min
`13.28` Session 7: Task 4: Maneuver: research filter adapter
`13.58` Session 8: Task 4: List Pasien Filter implementation
`14.28` Session 9: Task 4: List Pasien Filter debugging


## Decision
sebelum melakukan redesign filter, selesaikan minor bug terlebih dahulu. kemudian weekly task list 2. baru redesign.
