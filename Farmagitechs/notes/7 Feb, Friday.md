---
tags: ['2020/[02] February']
title: '7 Feb, Friday'
created: '2020-02-07T01:27:23.170Z'
modified: '2020-03-19T07:01:17.926Z'
---

# 7 Feb, Friday

`Day 69`
`Day 9 Aceh`

Kunjungan dari Rumah Sakit tetangga

Export Excel di SIMRS Report Temanggung. Sample ada di E-Doc.
Data di tampung di Document, sama seperti yang kubuat
- belum ada fungsi untuk membuat excel, fungsi serupa ada di E-Doc Utility
- format data yang dibutuhkan adalah List[List[String, Any]] class Result
- di Class Result[A], aku tidak tahu apa itu A
- membutuhkan class Document
- Tried get data via postman, which is require header or something.
- Cek api bisa langsung di web, formatnya gimana
- list terkecil rekap
- confusion with List[A], lets try with val

Step?
- membuat kelas dengan variable yang sama dengan parameter json, setidaknya data -> result.items
- generateExcel langsung dengan result.items. hasilnya gagal. type data found: List[_171] required : List[List(String, Any)]

## Log
`08.10` Datang


