---
tags: [Research/SIMRS]
title: Scratch Pad
created: '2019-11-26T00:55:27.431Z'
modified: '2020-01-27T03:37:33.103Z'
---

# Scratch Pad

- Menggunakan CodeIgniter
- Yang harus didokumentasikan
  - Modul-modul
  - Tables
  - Alur Program
  - Teknologi Apa saja yang digunakan
  - Sistem
- Tujuan pendokumentasian : agar pelacakan algoritma program mudah untuk dilakukan. Menemukan alur program yang redundant untuk diperbaiki di versi selanjutnya.
- Changelog dan Request Log
- Menggunakan metode Agile Development


## Modules `dc_module`
1. Sistem
2. Admission
3. Inventory
4. Master Data
5. Pelayanan
6. Lap. Pelayanan
7. keuangan
8. Akuntansi
9. Pelayanan Penunjang
10. Lap. Back Office
11. Tracer
12. Rekam medis
13. RL

```mermaid
graph LR

  0(SIMRS) --> 1(Sistem)
  0-->2(Admission)
  0-->3(Inventory)
  0-->4(Master Data)
  0-->5(Pelayanan)
  0-->6(Lap Pelayanan)
  0-->7(Keuangan)
  0-->8(Akuntansi)
  0-->9(Pelayanan Penunjang)
  0-->10(Lap Back Office)
  0-->11(Tracer)
  0-->14(Rekam Medis)
  0-->15(RL)
  
  1--> 03[Account]
  1-->073[Log]
  1-->0213[Admin Log]
  1-->0218[Master Data Log]
  1-->0235[Setting E-Prescription]
  1-->0237[Konfigurasi]



```
## Technical Requirements


