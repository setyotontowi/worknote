---
tags: ['2020/[02] February']
title: '21 Feb, Friday'
created: '2020-02-21T00:57:33.713Z'
modified: '2020-03-19T07:01:18.073Z'
---

# 21 Feb, Friday

`Day 77`
`Day 23 Aceh`

- [ ] SIMRS Abby: Installing Nilai Normal
- [x] FG-Report Temanggung: Print PDF: Setup


## Task 2
Sekilas:
Kemarin sudah download repo dan memasukkannya. Namun belum jalan. Lanjutkan setup.
Installing FG Resources

FG AUTH
/home/setyotontowi/Program/fg-auth/bin/fg-auth -Dhttp.port=9001 -Dconfig.file=/home/setyotontowi/Program/fg-auth/conf/application.conf  -J-Xms64M -J-Xmx196M

- Jalankan run.sh yang dari fg_auth program, bukan source code.
- Masukkan database auth_tmg

Jangan lupa setting direktori di run.sh

FG REPORT
fg_resources di htdocs
sbt run 9005

PDF: Dari html. 
- Bikin button dulu
- Data dari, mencontoh excel
- Print

Jembatan ke FG Printing Done.

## Log
`07.59` start working
`09.53` success installing
`12.02` success bridging.
