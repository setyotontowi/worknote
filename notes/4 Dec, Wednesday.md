---
tags: [2019/December]
title: '4 Dec, Wednesday'
created: '2019-12-04T00:24:11.780Z'
modified: '2019-12-05T00:28:09.679Z'
---

# 4 Dec, Wednesday

`Day 26`

- [X] 1. SIMRS V2.0 Margin Obat
- [ ] 2. SIMRS V2.0 Margin Obat Implementasi Ke Form

## Task 1
waiting for 100 becoming online
margin range
- [X] validasi bawah > atas (2)
      terdapat validasi dimana harga atas harus diisi. kemarin telah ditetapkan tidak harus ada batas atas
- [X] validasi perpotongan database (3) : 1. perpotongan rentang, 2. perpotongan nilai maksimal

```
select * from dc_margin_range where 120000 between range_bawah and COALESCE(range_atas, 120000)

select * from dc_margin_range where 100000 between range_bawah and COALESCE(range_atas, 100000) or 120000 BETWEEN range_bawah and COALESCE(range_atas, 120000)
```

- [X] pencarian (5) tidak perlu
- [X] reset atau reload belum bisa kemungkinan nabrak dengan kelas. reset dan reload berbeda
- [X] reload
- [X] if range atas null maka tampil bukan 0. bisa diganti seterusnya atau sebatasnya


margin kelas
- [X] validasi kelas yang sama (1)
      tujuannya adalah popup jika ada kelas yang sama. di database telah di set unique, namun penyajian ke usernya belum. apakah harus selalu melakukan pengecekan jika ada data yang sama? ya. tidak perlu alert untuk menimpa. tidak bisa ya tidak bisa. hold. yang penting sudah jalan dulu.

    - [X] bentuk pesannya.

- [X] pencarian (4) tidak perlu
- [X] reset

## Task 2

Menu yang diimplementasikan
1. Resep rawat jalan
2. resep rawat inap
3. penjualan bebas(non resep dan resep)
4. pemeriksaan klinik (kolom pemakaian bhp)
5. pemeriksaan IGD (kolom pemakaian bhp)
6. hail laboratorium
7. hasil radiologi
8. pemeriksaan rawat inap (pemakaian bhp)

### Random Notes

- rawat jalan masuk kelas yang mana
- ada harga margin rajal dan ranap, apakah dihiraukan atau margin dari margin_obat ditampilkan disitu..
- berarti perhitungannya ada di setiap menu yang menampilkan obat (beserta harganya dari hja)
- global settingnya

### Files
1. Rawat Jalan
`m_master_data/get_auto_barang_stok` untuk penghitungan hja

## Log
`07.18` datang
`08.00` read Agile Documentation
`09.48` start task 1
`14.10` task 1 done
`14.26` task 2 start, begin analysis
`16.03` pulang
