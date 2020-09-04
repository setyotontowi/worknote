---
tags: [2019/November]
title: '27 Nov, Wednesday'
created: '2019-11-27T01:45:36.673Z'
modified: '2019-11-27T07:16:21.652Z'
---

# 27 Nov, Wednesday

`Day 21`

- [X] 1. SIMRS Temanggung : Deskripsi Diagnosa LIS 
- [X] 2. SIMRS Temanggung : Tracer -> Distribusi Tracer
- [X] 3. SIMRS Dinda : Penambahan Keterangan Label IGD

## Task 1
1. `models/m_lis.php`

## Task 2

Tracer > Distribusi tracer
1. Kolom jeda sudah ada tetapi value nya belum muncul di hasil export
2. Penambahan kolom waktu berkas siap di hasil export
3. Penambahan judul hasil export Rekap Distribusi Tracer tgl dd/mm/yyyy s/d dd/mm/yyyy

**Files**

1. `controllers/tracer.php | distribusi_tracer`
2. `controllers/export.php | export_tracer`
3. `views/export/tracer/list_tracer.php` 
4. `models/m_tracer.php`

waktu jeda adalah order time dan ready time

## Task 3
**Files**

1. `views/keuangan/pembayaran/pembayaran_total.php`
2. `controllers/keuangan.php | rekap_billing_list_get`
3. `models/m_keuangan.php | get_list_rekap_billing`

karena jenis IGD belum ada datanya (yang tidak null) aku coba masukkan dulu di admisi IGD dengan data RM **107272, 107327, 107267**

perubahan sizeof (buang lagi setelah digunakan)
api/admission p. 1050
m_admission p. 659
m_pelayanan p. 1104


## Log
`07.19` Datang
`08.46` Various things, belajar bahasa jepang, konfigurasi ubuntu
`09.04` Task 1 Done, namun belum ditest
`09.49` Start Task 2
`10.51` Task 2 done
`14.15` Task 3 done
