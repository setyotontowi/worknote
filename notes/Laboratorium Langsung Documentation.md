---
tags: [Research/SIMRS]
title: Laboratorium Langsung Documentation
created: '2020-02-20T01:27:10.637Z'
modified: '2020-02-20T06:20:30.071Z'
---

# Laboratorium Langsung Documentation

On 
A. Pendaftaran
B. Entri Item Lab
C. Hasil Lab

### View in Main Page
1. List Pasien
   API: api/pelayanan_non_rm/pendaftaran_non_rm_list/
    param: page/1/jenis/Laboratorium
    URL Encoded: awal, akhir, no_register, no_rm, nama, id

    awal:20/02/2020
    akhir:20/02/2020
    no_register:
    no_rm:
    nama:
    id:

### Pendaftaran
1. Cari RM
   API: api/admission_auto/pasien_auto
   di fungsi $('#no_rm').select2()
 
2. Advanced Search Pasien
   API: api/admission/pasien_list/
    param: page/1
    URL Encoded: no_rm, nama, kelamin, umur, alamat, telp
   
3. Kelurahan
   API: api/masterdata_auto/kelurahan_auto

4. Perujuk

### Transaction in Entri Item Lab

1. Tampil All Data Pasien
2. Entri Item Lab
3. Simpan Request Lab

### Transaction in Hasil Lab
1. Dokter
2. Cetak Hasil
3. Entri Hasil
4. BHP
