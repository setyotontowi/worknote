---
tags: ['2020/[01] January']
title: '3 Jan, Friday'
created: '2020-01-03T01:35:43.359Z'
modified: '2020-03-19T07:01:59.118Z'
---

# 3 Jan, Friday

`Day 45`

- [ ] 1. SIMRS Dinda : Bug laboratorium

## Task 1

Penunjang/Daftar Lab

Kalau tidak salah daftar item yang dipilih tidak muncul semuanya. Sebagai contoh. item hematologi yang dipilih ada hemoglobin dan leukosit. namun yang muncul hanya hemoglobin saja dengan nilai normalnya. 

cek : apakah masuk di dc_item_detail_lab?

file yang aku ubah : m_pelayanan/get_item_

permasalahan utama filter : 
dia akan langsung menampilkan item dan nilai_normalnya. jadi ketika nilai normal tidak masuk di where manapun, item tidak akan tampil sama sekali.

istilah : //get id_detail_lab used in foreach = query 1

algoritma original sebelum aku main main disana :
dia akan mengambil id_detail_lab yang di grup (berarti 1 id) dan mengambil item dengan lab id itu. syntax foreach yang ada di bawahnya benar-benar tidak berguna. 

algoritma yang aku ajukan : 
penyortiran item lab akan dilakukan di query 1
query 2, atau yang ada di foreach akan memfilter nilai normalnya

verifikasi : ya. algoritmanya berantakan. di sini : //get id_detail_lab used in foreach
yang bertujuan untuk hanya mengambil id_detail_lab, sama saja. 

solusi : algoritma yang diajukan

**Note**

Ada sekitar 4 file yang akan terpengaruh. 

## Log
`07.27` datang
