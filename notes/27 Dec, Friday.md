---
tags: [2019/December]
title: '27 Dec, Friday'
created: '2019-12-27T00:30:24.829Z'
modified: '2019-12-30T01:39:05.046Z'
---

# 27 Dec, Friday

`Day 41`

- [ ] 1. SIMRS Tangerang : Resep gizi
- [X] 2. Update To Dinda Testing

## Task 1

Kata mas arvin, fokus ke task no 2 dulu di trello. Namun aku menemukan bahwa ada tabel yang tidak ada di mas joko.

mengubah nama dc_order_gizi menjadi dc_order_jenis_diet (salah, bukan ini)

restart untuk masuk ke vpn

Connect/Konek ke Tangerang
VPN, 
192.168.10.81

password phpmyadmin ramenrider

---
This is the init problem.
Butuh penyesuaian beberapa tabel dalam database. Sudah aku ubah programmatically di source code. get_list_history_order_gizi()

ada tiga tabel yang terlibat
1. dc_gizi_jenis_diet
2. dc_order_gizi
3. dc_order_jenis_diet (ini baru, yang bertujuan untuk menampung agar tidak error : defaultnya tidak ada)

---
Problem kedua : fungsi konfirmasi_order_gizi ga ada di api/pelayanan
Problem ketiga : format etiket tidak sesuai dengan data yang ada


## Task 2

1. Create Table

```sql
CREATE TABLE `training_simrs`.`dc_kategori_nilai_normal` ( 
  `id` INT NOT NULL AUTO_INCREMENT , 
  `nama` VARCHAR(50) NOT NULL , 
  `awal` DOUBLE NULL , 
  `akhir` DOUBLE NULL , 
  `jenis` ENUM('Hari','Bulan','Tahun') NULL , 
  `kelamin` ENUM('L','P') NULL , 
  PRIMARY KEY (`id`)) ENGINE = InnoDB
```

2. Add Default Value in kategori_nilai_normal

3. Change struktur kategori in dc_nilai_normal_lab to int FK

4. Change all data in kategori related in kategori_nilai_normal

5. Add menu

```sql
select *, 
if(kategori="L", "1", if(kategori="P", "2", if(kategori="A","3",null))) as kat_nn
from dc_nilai_normal_lab
```

## Log
`07.25` datang
`10.10` idle
`11.10` modifying database
`16.19` pulang
