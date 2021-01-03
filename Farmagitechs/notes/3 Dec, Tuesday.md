---
tags: [2019/December]
title: '3 Dec, Tuesday'
created: '2019-12-03T00:21:40.620Z'
modified: '2019-12-03T08:51:03.420Z'
---

# 3 Dec, Tuesday

`Day 25`

- [ ] 1. SIMRS V2.0 Margin Obat

## Task 1
Tampilan

tampilan seperti masterdata yang lainnya. Ada dropdown list yang membedakan range dan kelas. tentu saja ada tambah marginnnya. Kita akan menambahkan satu data ke dua tabel tersebut, terus membuat modelnya.

### Range
controllernya api, javascript get_list_margin
1. dropdown
    sample ada di pelayanannonrm/print_label_gizi
2. tabel
    sample ada di masterdata/komponen_tarif
    ada dua master data nantinya, untuk range dan kelas
3. javascript

- untuk range validasi, apakah udah ada value di range tersebut.

break 1
- pagination masih belum jalan, di model start limitnya di set. done
- apakah setelah data terinsert, tampilnya di yang pertama atau terakhir? done
- edit dan hapus belum bisa done
- mengganti semua alur. controller api dan model benar-benar dipecah menjadi 2 done

hold 2 
- validasi bawah > atas
- validasi perpotongan pada database
- pencarian
- reset

### Kelas
- create done
- delete done
- edit, select2 select done
- pencarian
- reset

## Log
`07.12` datang
`08.24` task 1
`09.43` get data
`10.58` margin range tampil
`13.43` mengganti semua alur
`14.20` margin range done
