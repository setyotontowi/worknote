---
tags: [2019/December]
title: '18 Dec, Wednesday'
created: '2019-12-18T01:12:34.302Z'
modified: '2019-12-18T09:01:46.188Z'
---

# 18 Dec, Wednesday

`Day 35`

- [X] 1. SIMRS Dinda : new Masterdata
  - [ ] 1.1 Revisi : filtering nilai normal di hasil lab. 
- [ ] 2. SIMRS Temanggung : log masterdata

## Task 1
status sekarang, simpan, update dan delete belum.
- [X] Masterdata. 
- [X] Hasil Lab
- [X] Item lab

Perubahan Database
- new table
- change structure kategori into fk from enum (L, P, A)

Hasil lab
nilai normal sudah muncul begitu saja. filter nilai normal dilakukan melalui item laboratiroum
pertama kali dia ambil dari dc_detail_lab.id untuk diambil di dc_item_detail_lab

## Task 2

List Function (m_masterdata)
- ICD X : update_data_golongan_sebab, delete_data_golongan_sebab `done`
- Gizi : save_data_barang_no, delete_data_barang
- Barang PF (Farmasi) : save_data_barang(), delete_data_barang()
- Barang Rumah Tangga : save_data_barang_no(), delete_data_barang() //barang sama, menu berarti juga sama (Barang PF, Gizi)
- Expertise : update_data_expertise(), delete_data_expertise()
- Farmako Terapi : update_data_farmako_terapi(), delete_data_farmako_terapi()
- Instansi : update_data_instansi(), delete_data_instansi()


## Log
`07.30` datang
`10.47` task 1 all done
`13.14` dari barang rumah tangga sampai ke instansi
`13.49` idle
`16.01` pulang

## Random Notes

- menggunakan vue js dibandingkan dengan menggenerate html via javascript
