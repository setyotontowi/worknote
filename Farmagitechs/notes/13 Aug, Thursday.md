---
tags: ['2020/[08] August']
title: '13 Aug, Thursday'
created: '2020-08-13T00:24:12.251Z'
modified: '2020-08-13T08:09:54.248Z'
---

# 13 Aug, Thursday

`Day 202` Doesn't matter, do something!

## Early notes
Allright, we back to SIMRS V2 Project after, perhaps in a month, we struggle with Android stuff everyday. On the beginning, we have to adapt on the environment, set the configuration, update the repos and databases, then we can learn on what task we assigned. 

And yeah, I propose that we should do an early and late learning for an hour each. We can use sites like medium, reddit, or quora to add insight. 

So, Today
- [x] SIMRS V2: Configuration
- [x] SIMRS V2: Copy `Verifikasi Kwitansi` to `Bendahara` menu `OrbygCcC`
- [x] SIMRS V2: Then add button/function export to excel
- [x] SIMRS V2: Revision, separate status in the other column.
- [x] SIMRS V2: Publish

## Task 1
Uhuh. we completely forget about this. So what's the plan for this?
- [x] updating the repos

Verifikasi Jurnal, we didn't know what database should be. Perhaps, check live first.
- [x] set database to 100, our server. also, see history.sql
Findings: there is `verifikasi kwitansi`. but our local simrs directs it to `verifikasi jurnal`. Maybe, the menu url not match with live database. should check first. 

## Task 2
remember to checkout to dev branch.
- controllers/akuntansi/verifikasi_kwitansi
- views/akuntansi/verifikasi_kwitansi

copy those files to something related to bendahara
```sql
-- Add Menu in Bendahara
INSERT INTO `dc_privileges` 
(`id`, `id_module`, `menu`, `url`, `icon`, `urutan`, `active`) 
VALUES (NULL, '15', 'Rekap Pembayaran Pasien', 'keuangan/rekap_pembayaran_pasien', 'fa-check-circle', '3', '1');
```

## Task 4
a fresh start
- [x] separate col, with default content button like text
- [x] restore query generator
- [x] search by status. only in bendahara

## Task 5
- [x] update to repo live, merge first and delete branch
- [x] update history.sql
- [x] update to live
- [x] update database each, after update
- [x] update database testing

on hospital
- [x] PKU Purbalingga
- [x] Klinik Merden (lemot)
- [x] RSGM
- [x] PKU Banjar

## Logs
`07.10` init
`08.32` early learning complete
`10.19` task 1 complete
`10.42` task 2 complete
`11.31` task 3 complete total 3 hours since `08.32`
`13.07` after long break
`14.12` task 4 complete total 1+05 hours since `13.07`
`14.49` task 5 complete

