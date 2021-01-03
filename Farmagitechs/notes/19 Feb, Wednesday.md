---
tags: ['2020/[02] February']
title: '19 Feb, Wednesday'
created: '2020-02-19T01:35:47.214Z'
modified: '2020-03-19T07:01:18.008Z'
---

# 19 Feb, Wednesday

`Day 75` Cuti 2 Hari
`Day 21 Aceh`

- [ ] SIMRS V2 : installing nilai normal

## Task 1 
- Setup, installing SIMRS Dinda.
- Setup, installing SIMRS V2, copying from hardisk.

Beberapa mungkin sudah selesai. Karena hamachinya error, mungkin perlu kita test sendiri. Juga, dokumentasi. Kita masih punya dua atau tiga hari, kan?

Skenario Testing, Per Menu
1. Menu Kategori Nilai Normal
2. Menu Item Laboratorium
3. Menu Pelayanan Penunjang - Laboratorium Langsung
4. Menu Pelayanan - Entri Laboratorium
5. Menu Pelayanan - Hasil Laboratorium

#### Menu Kategori Nilai Normal
- [x] Insert
      1. Insert, rentang seharusnya di bawah kolom usia
      2. Insert, rentang harusnya di disabled ketika pilih jenis usia
- [X] Update 
- [X] Delete 

#### Menu Item Laboratorium
Khusus untuk kategori nilai normal
- [x] Insert
    1. Kategori menggunakan autocomplete?
- [x] Update
- [x] Delete

#### Menu Laboratorium Langsung
1. Entri Item

- Setelah tambah item, tanggal_lahir dan jenis_kelamin tidak ikut terambil.
  ini masalah query yang tidak ada jenis kelaminnya. query pengambilan jenis kelaminnya ada di m_pelayanan/get_pemeriksaan_laboratorium. Ini merambah ke mengapa item lab tidak muncul di hasil laboratorium.



## Log
`08.38` start working
