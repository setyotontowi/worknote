---
tags: ['2020/[05] May']
title: 'May 12, Tuesday'
created: '2020-05-12T00:51:49.561Z'
modified: '2020-05-12T07:48:31.505Z'
---

# May 12, Tuesday

`Day 140` Stiffness

- [x] SIMRS V2: List tindakan dijadikan satu dengan total jumlah di rincian billing: c/ixl5cRbj
- [x] SIMRS V2: validate count(*) as frekuensi di beberapa fungsi: may 11
- [ ] SIMRS V2: Operasi IGD /c/ahE4r6Dy/ : may 11
- [x] SIMRS V2: Error tambah hemodialisa: parent->task 2
- [ ] SIMRS V2: Tagihan rawat inap ke double: c/Xi9gCVP1

## Task 1

**Note**
Setelah berbicara dengan mas arvin, query tampilannya sudah dibenerin sesuai dengan instruksinya. permasalahannya ada ketika cetak dan tampilan menggunakan query yang sama, khususnya terletak di group by waktu. di cetak, group by waktu akan diabaikan

**Fungsi**
- m_keuangan: get_tarif_tindakan_list

> Solution
  pada cetak, group by waktu dihilangkan. itu berarti membuat variable $p baru untuk menyeleksi apakah request berasal dari cetak atau tampilan

**Warning**
about mongo db, check first as always


## Task 2
Bagaimana alur pengecekannya?

**Fungsi**
- get_tarif_operasi_list
- get_tarif_hemodialisa_list
- get_tarif_laboratorium_group
- get_tarif_radiologi_group
- get_tarif_fisioterapi_group
- tagihan_tindakan
- tagihan_operasi

**Problem**
dalam beberapa hal seperti hemodialisa, lab, rad, fisio, kemo qty tidak mungkin dilakukan. namun item layanan bisa jadi dua kali diinput bersamaan. di dalam tampilan sum qty memang tidak berpengaruh dan tetap dibiarkan apa adanya dengan group by waktu. namun di cetak, tetap group by waktunya dihilangkan.


**Note**
1. Radiologi, di fungsi tersebut: done
2. Laboratorium sudah di grouping: done
3. Hemodialisa, onhold
4. Fisioterapi belum di cek

> Onhold
  Partially completed since it's not obligatory, waiting for next update if any task added in trello. 

## Task 4

**Problem**
Cannot add or update a child row: a foreign key constraint fails 

> On Hold
Sementara ini, karena belum ada konfirmasi apakah itu bug atau sebuah salah langkah, maka tindakan yang paling tepat untuk saat ini adalah ditunda

## Task 5
**Problems**
menghilangkan akomodasi rawat inap di tindakan.

**Menu**
1. Rincian Billing
2. Pembayaran


## Logs
`07.52` start
`09.30` task 1 done
`10.43` start task 2
`12.27` task 2, 2 fungsi selesai.
`14.26` task 2, 4 dianggap selesai. commit setelah maya sudah testing. jangan lupa kembalikan logdata.

