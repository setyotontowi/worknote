---
tags: ['2020/[01] January']
title: '28 Jan, Tuesday'
created: '2020-01-28T01:54:32.558Z'
modified: '2020-03-19T07:01:59.595Z'
---

# 28 Jan, Tuesday

`Day 61`

- [ ] SIMRS V2 : Kategori Nilai Normal : Penambahan di 3 menu

## Task 1

File yang terlibat
1. views/penunjang/entri_laboratorium
2. views/penunjang/hasil_laboratorium
3. views/penunjang/laboratorium_form2
4. views/pendaftaran_non_rm/pendaftaran/laboratorium_langsung 
5. views/printing/penunjang/hasil_laboratorium
6. views/export/pelayanan/export_hasil_lab 
7. controllers/api/masterdata
8. controllers/api/pelayanan
9. controllers/export
10. controllers/masterdata
11. controllers/printing
12. models/m_masterdata
13. models/m_pelayanan

---

**models/m_pelayanan**
1. get_item_pemeriksaan_laboratorrium
2. cetak_pemeriksaan_laboratorium_detail

**models/m_masterdata**
1. reset_nilai_normal
2. update_nilai_normal_lab
3. get_nilai_normal

**controllers/api/masterdata**
1. nilai_normal_laboratorium_post
2. create read update delete function

**controllers/api/pelayanan**
1. hasil_laboratorium_save_post
2. permintaan_pemeriksaan_laborataroium_get

**controllers/export**
1. export_hasil_laboratorium

**controllers/masterdata**
1. kategori_nilai_normal

**controllers/printing**
1. hasil_laboratorium

**+ export_hasil_lab**

---

## Log
`07.40` datang
`08.55` start working
`10.31` check point, all controller - models
`10.50` all modules done.

