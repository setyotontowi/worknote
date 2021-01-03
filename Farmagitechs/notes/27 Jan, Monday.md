---
tags: ['2020/[01] January']
title: '27 Jan, Monday'
created: '2020-01-27T02:27:37.622Z'
modified: '2020-03-19T07:01:59.571Z'
---

# 27 Jan, Monday

`Day 60`

- [ ] SIMRS V2. Installing Kategori Nilai Normal
- [ ] Scala : dataflow through model

## Task 1
__Alur level database (yang digunakan lokal : klinikpkumerden)__
1. Bikin table baru 'dc_kategori_nilai_normal'

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

2. Insert Default Value in `dc_kategori_nilai_normal`
    1. Laki-Laki
    2. Perempuan
    3. Anak 0-5 Tahun

```sql
INSERT INTO `dc_kategori_nilai_normal` (`id`, `nama`, `awal`, `akhir`, `jenis`, `kelamin`) 
VALUES 
(NULL, 'Laki-laki', NULL, NULL, NULL, 'L'), 
(NULL, 'Perempuan', NULL, NULL, NULL, 'P'), 
(NULL, 'Anak', '0', '5', 'Tahun', NULL)
```

3. Alter table di dc_nilai_normal_lab
    1. Ubah Tipe data 'kategori' dari enum ke varchar
    2. Ubah data dimana L menjadi 1, P menjadi 2, A menjadi 3. Serupa dengan id yang ada di `dc_kategori_nilai_normal`
    3. Ubah Tipe data 'kategori' dari varchar ke int
    4. Tambahkan relasi 'kategori' dengan 'dc_kategori_nilai_normal'.'id'


  ```sql  
  #1
  ALTER TABLE `dc_nilai_normal_lab`   
  CHANGE `kategori` 
  `kategori` VARCHAR(25) 
  CHARACTER SET latin1 COLLATE latin1_swedish_ci NULL DEFAULT NULL;

  #2
  UPDATE dc_nilai_normal_lab SET kategori = 1 WHERE kategori = 'L'
  UPDATE dc_nilai_normal_lab SET kategori = 2 WHERE kategori = 'P'
  UPDATE dc_nilai_normal_lab SET kategori = 3 WHERE kategori = 'A'

  #3
  ALTER TABLE `dc_nilai_normal_lab` CHANGE `kategori` `kategori` INT(11) NULL DEFAULT NULL;

  #4
  ALTER TABLE `dc_nilai_normal_lab` 
  ADD CONSTRAINT `dc_nilai_normal_lab_ibfk_2` 
  FOREIGN KEY (`kategori`) REFERENCES `dc_kategori_nilai_normal`(`id`) 
  ON DELETE CASCADE ON UPDATE CASCADE;
  ```

4. Insert menu baru untuk master data kategori nilai normal

__Alur level Aplikasi__
1. Bikin menu baru
   controllers masterdata, api masterdata, views kategori_nilai_normal, models m_masterdata
2. Perubahan di menu item lab
3. Perubahan di menu pelayanan entri lab
4. Perubahan di menu pelayanan hasil lab
5. Perubahan di menu pelayanan penunjang order lab


## Log
`07.33` datang
`09.28` ngobrol dan basa basi senin pagi
`11.35` menu kategori_nilai_normal, menu item_lab

