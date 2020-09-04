---
tags: ['2020/[06] June']
title: '18 Jun, Thursday'
created: '2020-06-18T00:39:36.682Z'
modified: '2020-06-26T14:03:20.526Z'
---

# 18 Jun, Thursday

`Day 162` Grokking The System

- [x] E-Doc: Revisi 3.1: Problem 3: Parent -> 17 Jun
- [x] E-Doc: Revisi 3.1: Problem 2: Parent -> 17 Jun
- [x] SIMRS V2: Penambahan Rule Nilai Normal: Push: Parent -> 12 Jun PAYfih1T
- [x] E-Doc: Revisi 3.1: Problem 2: Revisi: Parent -> Task 2
- [ ] E-Doc: Side Quest: Redesign: Parent -> 10 Jun
- [x] SIMRS V2: Hasil Lab pdf tidak keluar di Testing, padahal di lokal keluar: Parent -> Task 3

## Task 1
- Skenarionya, setelah klik dia muncul dialog seperti list type document. 
- jika ingin menambahkan id dokter, maka harus menggunakan class dokter.

## Task 3
For Every Hospital
1. RSGM (done, test and live)
2. PKU Merden (done, test and live)
3. Klinik Merden (done)
4. PKU Purbalingga (done, both)
5. Mas Joko (done)

- alter table
```sql
ALTER TABLE `dc_nilai_normal_lab` 
CHANGE `operator` `operator` 
ENUM('-','<','<=','>','>=','Positif','Negatif','Reaktif','Non Reaktif')
```
- branching dev_owi (unable)
- push server (1,2,3,4)

## Task 5
Previously in 16 Jun
Calendar View: ini tidak bisa digunakan karena tidak ada method setCurrentPosition

**Decision**
- move to this https://github.com/Mulham-Raee/Horizontal-Calendar

## Task 6
**Problem**
- khusus print dan ekspor, hasil lab tidak keluar. namun dalam sistem berjalan dengan baik termasuk dengan normal dan abnormalnya. di lokal juga tidak ada masalah yang terjadi.

**Hipotesis**
- ada masalah terkait dengan databasenya.

**Todo**
- change to database mas joko

## Logs
`07.17` init
`08.10` Session 1: Task 1: First Stage Coding
`08.40` Session 2: Task 1: Second Stage Coding
`09.10` Session 3: Task 1: Third Stage Coding: SharedPref
`09.40` Session 4: Task 1: Fourth Stage Coding: Dokter Adapter : Alfamart
`10.20` Session 5: Task 1: Fifth Stage Coding:
`11.04` Interlude: Push Repo (fin)
`12.45` Session 6: Task 1: Fixing The Adapter Bug: (fin, with revisi (task 4))
`13.15` Session 7: Task 2: Calendar View, The Analysis
`13.50` Session 8: Task 2: Moving to Horizontal Calendar
`14.20` Session 9: Task 6: Debugging
`14.50` Session 10: Task :
