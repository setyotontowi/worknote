---
tags: ['2020/[01] January']
title: '2 Jan, Thursday'
created: '2020-01-02T01:30:20.315Z'
modified: '2020-03-19T07:01:59.070Z'
---

# 2 Jan, Thursday

`Day 44`

- [ ] 1. SIMRS Dinda : Menampilkan item laboratorium semuanya.
- [X] 2. SIMRS Klinik PKU Merden : Preparation [link](https://trello.com/c/yXfgPuLa/24-hasil-testing-klinik-pku-merden)

## Task 2
- subtask 5
error ada di fungsi api/pelayanan/permintaan_pemeriksaan_radiologi_get : berbeda dengan di SIMRS versi 1. kemungkinan errornya sama dengan laboratorium kemarin. tidak masuk di dc_laboratorium. go to database. permasalahannya ada di api/pelayanan/order_radiologi_post. ada sesuatu di comment disitu. jika ingin mencari, keywordnya : `considered a bug in Entri Radiologi`

- subtask 6  : loading lama ketika meload `api/penunjang/get_bhp_laboratorium/id_laboratorium/10` query di sini, return null. maka loadingnya tidak pernah berhenti dan tidak pernah kesimpan. problem. summernote things. at save_data_hasil_lab() in laboratorium_langsung

- subtask 1 : empty dc_bank
- subtask 9 : wrong parameter. expected no_rm, but found unknown id
- subtask 8 : see comment in code

## Log
`07.30` datang
`08.30` start task 2
`09.27` task 2 subtask 5 done
`13.48` task 1 & 6
`14.27` task 9
`14.37` task 8
`16.14` pulang


