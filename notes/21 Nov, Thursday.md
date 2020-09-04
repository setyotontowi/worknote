---
tags: [2019/November]
title: '21 Nov, Thursday'
created: '2019-11-21T00:43:36.388Z'
modified: '2019-11-21T07:52:13.556Z'
---

# 21 Nov, Thursday

`Day 17`

- [X] SIM RS Dinda
  - [X] Revisi : Filternya ga nyampe, tanggal di set hari ini (pushed)
- [ ] SIM RS Temanggung 
  - [X] Kertasnya kepanjangan, spacenya dikecilkan
  - [ ] Penambahan Etiket di BDRS
- [ ] Dokumen High Alert Medication  


## Task 1
- mengecek seluruh alur loginnya. kenapa session tidak ditaruh di setiap login. apa, ketika kita login, kan ada tuh milih unit dan disimpan di cache. maka maksudnya setelah unit itu disimpan kan?

The beginner starts to get frustrated

- Login algorithm
```
0. Default route controllers/app.php
   disini akan dicek apakah user id udah di set dalam session apa belum. 
   jika sudah maka akan diarahkan ke dashboard. 
   jika belum akan dicek lagi apakah terdapat getter dari token. 
   jika belum maka akan di arahkan ke halaman login
1. controllers/app.php login()
2. views/login.php
3. mengecek jadwal shift di views/login.php cek_shift()
4. views/login.php logmein()
5. controllers/users logmein() session di set
6. models/m_users validate_my_account()
7. die in controllers/users logmein()
```

- login sudah berhasil. jabatan juga sudah terisi statis sepertinya. tapi ketika user depeka memilih unit di dashboard, tetap saja itu tidak terupdate

- Log Login Algorithm
```
1. input ke dc_session ketika controllers/users logmein() atau setelah session di set
2. id_login session di set dengan mengambil data terakhir yang diinputkan
3. ketika memilih unit di dashboard, maka ketika session unit di update oleh sistem, unit di dc_session juga diupdate dengan parameter id_login
```
---

## Random Notes
1. darimana session id_group
2. tujuannya adalah mengetahui kenapa dc_session diisi setelah token ada? ataukah setiap kali user login maka lognya akan tercatat? ada session id_unit ketika , tapi itu masih berelasi dengan masterdata.
3. **penting** sebelum di push, comment di app di nonaktifkan

## Log
`07.33` Datang
`09.23` Analisis algoritma login
`09.58` statis jabatan, unit belum
`10.16` unit sudah, username di auto belum
`10.23` all module done
`11.29` task 2 done
`13.10` revisi task 1 done
`14.00` dokumentasi android
`14.39` idle
`14.52` setting up android
