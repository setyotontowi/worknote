---
tags: ['2020/[06] June']
title: '30 Jun, Tuesday'
created: '2020-06-30T00:47:38.043Z'
modified: '2020-07-01T13:09:39.931Z'
---

# 30 Jun, Tuesday

`Day 170` End of month

- [x] 1. SIMRS V2: Upload Nilai Normal -> 29 Jun
- [x] 2. E-Doc: Revisi 3: Dismiss Dialog Dokumen: XpIRw0zp: onHold
- [x] 3. E-Doc: Revisi 3: Scroll view di dokumen history neFIWaIP
- [x] 4. E-Doc: Revisi 3.3: Refreshview di Pasien Fragment -> Task 3
- [x] 5. E-Doc: Revisi 3.3: Toggle menu button di dokumen activity -> Task 3
- [x] 6. E-Doc: Revisi 3: Tombol Back di halaman utama tidak berfungsi 61kqgokj
- [x] 7. E-Doc: Revisi 3: Notifikasi/Label saat Zoom/Edit dokumen eedx8WmW
- [x] 8. E-Doc: Revisi 3: Penambahan Label pada cards pasien adHiBdfn
- [x] 9. E-Doc: Revisi 3: Add logout button e9T80HcS
- E-Doc: 4th Stage: Migrate to MVVM and Butterknife
- E-Doc: MenuItem visibility dibuat method -> Task 5
- Learn Fragment Manager and Fragment Support Manager

`10.16` tampaknya akan menyenangkan jika aku menghabiskan hari ini dengan migrating ke butterknife dan mvvm.

## Task 1
- Abnormal di hasil lab. finish, in 3 view: `hasil_laboratorium`, `laboratorium_form2`, `laboratorium_langsung`.
- Rule Reaktif - Non Reaktif. finish in `m_masterdata/get_operator`
- penambahan enum di database table: `dc_nilai_normal_lab` col operator. finish

**Database To 4 Hospitals**
- PKU Purbalingga : fin, testing-live
- Klinik Merden :  fin, live
- RSGM : fin, testing-live
- Banjar : fin, testing-live

**Source Code to 4 Hospitals**
- PKU Purbalingga : fin
- Klinik Merden : fin
- RSGM : fin
- Banjar : fin

## Task 2
jadi setelah dokumen ditampilkan dan kembali, dialognya masih muncul. 

**Status**
On Hold. karena diganti dengan penambahan aktivitas baru.

## Task 3
**Status**
belum di test

## Task 4
- contohnya ada di class ListPasienFragment

## Task 5
- Toggle button edit, atau zoom (lebih tepatnya hand aja). dengan toast yang menandakan dia aktif atau tidak. ada dua mode, zoom: yang muncul hanya search. sedangkan edit: undo, redo, brush mode. 
- dokumen ada di DocumentActivity dengan menu_document. maka cari dimana toggle buttonnya aktif. sehingga hide/display menu juga akan ikut dieksekusi.

## Task 6
**complete**
onBackPressed in main activity

## Task 7
**todo**
using toast

**complete**
somehow, toast didn't work using ActionBar set title instead

## Note 1. 
- using some libraries. but they're available only in kotlin.

```java
viewModel = new SomeClassViewModel()
```

## Logs
`07.07` Init
`08.12` Session 1: Task 1: Waiting for Connection
`09.07` Session 2: Task 2,3: Giving conclusion
`09.26` Session 3: Task 5,4: complete, all
`09.43` Session 4: Task 6,7: complete, all
`11.18` learning mvvm
`14.39` introduction to mvp and mvvm
