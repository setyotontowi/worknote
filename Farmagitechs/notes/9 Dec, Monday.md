---
tags: [2019/December]
title: '9 Dec, Monday'
created: '2019-12-09T00:41:51.705Z'
modified: '2019-12-09T09:03:41.815Z'
---

# 9 Dec, Monday

`Day 29`

- [ ] 1. SIMRS V2.0 bug

## Task 1
1. Resep rawat jalan
2. resep rawat inap
3. penjualan bebas(non resep dan resep)
4. pemeriksaan klinik (kolom pemakaian bhp)
5. pemeriksaan IGD (kolom pemakaian bhp)
6. hail laboratorium
7. hasil radiologi
8. pemeriksaan rawat inap (pemakaian bhp)

Analisis
permasalahannya adalah penghitungan ulang dilakukan di database. (resep rawat jalan, resep rawat inap). main model. 
tidak ada perbedaannya insert resep rajal/ranap. insertnya dari kelas.
edit, dia ngambil di database resep, jadi pasien tidak ada kelasnya.
id_kelas sudah di sent
ranap :
rajal :

penjualan bebas -> ketika di tambahkan harganya berbeda. (hold) main javascript? penjualan bebas juga ada dari RM. tapi tidak berpengaruh kepada opsi margin. yang diberlakukan adalah margin rajal. (done)

pemeriksaan klinik, pemeriksaan IGD, pemeriksaan rawat inap form pemakaian BHP ketika ditambahkan berbeda main javascript?

- [X] resep ranap
  - [X] dari form_resep 4
  - [X] dari resep_ranap 6
- [X] resep rajal
  - [X] edit
  - [X] tambah
- [X] penjualan bebas
- [X] pemakaian bhp
- [ ] bug entry pemeriksaan lab, return dari database 0

bug entry bhp pemeriksaan lab, 

### Notes to do

- pengecekan setiap menu, apakah parameter kelas dikirimkan.
- insert obat resep di model save_resep_rsutemanggung juga belum dibuat marginnya.  
- perbandingan get_list_data_resep_asli

## Log
`07.25` datang 
`08.13` start task 1
`09.56` penjualan bebas, done
`10.57` resep rajal edit done, resep ranap edit tinggal tambah kelas di view
`11.18` break
`12.40` start
`14.11` rajal bug, ranap done
`14.34` bhp done
`16.15` pulang

