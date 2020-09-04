---
tags: ['2020/[04] April']
title: 'Apr 28, Tuesday'
created: '2020-04-27T23:45:24.092Z'
modified: '2020-04-28T09:14:42.155Z'
---

# Apr 28, Tuesday

`Day 133`

- [x] Phpmyadmin
- [ ] SIMRS V2: Entri Laboratorium: https://trello.com/c/cmvfFhIO/
- [ ] SIRMS V2: Issues 1

What are we gonna do?

## Task 1
reconfiguring database. i'm using different mysql service. 
Expect: mysql from ubuntu - phpmyadmin from xampp
Current: msyql from xampp - phpmyadmin from xampp

controluser somehow salah. 
mysql -u setyotontowi -p 2504 itu benar dan bisa masuk.

sampai sekarang analisanya mungkin dari permasalahan socket? tapi tadi ketika dicoba tetap tidak bisa. 

(hipotesis 1)
- pma__userconfig hanya menyimpan konfigurasi user.
- user yang digunakan berada di mysql.user;

sejauh ini hipotesis 1 belum bisa dibenarkan

(hipotesis 2)
- tidak bisa connect dengan mysql

eventually, I give up. so I'm using fully xampp to operate all repos. Which is likely unacceptable because it run in former php version. 



## Logs
`06.00` start
