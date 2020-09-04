---
tags: [2019/December]
title: '2 Dec, Monday'
created: '2019-12-02T00:41:59.610Z'
modified: '2019-12-10T05:39:56.134Z'
---

# 2 Dec, Monday

`Day 24`

- [X] 1. Learn Kotlin
- [X] 2. PKU Merden
- [X] 3. SIMRS Temanggung Deploy Server setelah dhuhur
- [ ] 4. SIMRS V.2 Margin Penjualan Obat Per Kelas dan Range

## Task 2

Resep Rawat Inap bukan yang setelah pulang. itu berbeda. Yang jadi masalah adalah menampilkan tabs riwayat resep.

permasalahannya strukturnya beda antara pku merden dan simrs v2. datamodal_penjualan bagian modal body berbeda.

Meskipun memang ada filenya, namun strukturnya bisa berbeda. ada beberapa file yang serupa namun aku tidak tahu mana yang harus dipakai

ternyata reponya salah

## Task 4
Pembuatan menu masterdata margin. Deadline Rabu, atau Kamis. Di Database buat dua tabel berdasarkan kelas dan range. untuk kelas, per kelas akan di set biaya per kelas kena margin berapa. ada juga skenario menggunakan range harga. jadi untuk harga obat sekian hingga sekian akan dikenakan margin berapa. 

- yang kena margin adalah harga hpp
- perhitungan obat akan ditentukan ketika resep diinisiasikan untuk pasien. hpp * margin
- untuk pengidentifikasian menggunakan range atau kelas, menggunakan global setting. jadi ketika global setting di set menggunakan range, margin di kelas tidak akan pernah dipakai. and vice versa. ada di dc_settings atau semisalnya.

1. Buat Tabel, 2 tabel
2. Buat Menu
3. DC Settings, ini terakhir tanya penerapannya seperti apa. inisiasinya dimana
4. Analisis Penggunaan Resep

Tabel
1. dc_margin_kelas [id, id_kelas, margin]

```
CREATE TABLE `dc_margin_kelas` ( 
`id` INT NOT NULL AUTO_INCREMENT , 
`id_kelas` INT NOT NULL , 
`margin` INT NOT NULL , 
PRIMARY KEY (`id`)) ENGINE = InnoDB;
```

2. dc_margin_range [id, harga_bawah, harga_atas, margin]

```
CREATE TABLE `dc_margin_range` ( 
`id` INT NOT NULL AUTO_INCREMENT , 
`range_bawah` INT NOT NULL , 
`range_atas` INT NOT NULL , 
`margin` INT NOT NULL , 
PRIMARY KEY (`id`)) ENGINE = InnoDB;
```

3. dc_margin_option
```
CREATE TABLE `dc_margin_option` (
  `id` int(11) NOT NULL,
  `opsi_margin` enum('Layanan','Kelas','Range') NOT NULL,
  `default_kelas_margin_rajal` int(11) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

ALTER TABLE `dc_margin_option`
  ADD PRIMARY KEY (`id`),
  ADD KEY `default_kelas_margin_rajal` (`default_kelas_margin_rajal`);
ALTER TABLE `dc_margin_option`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=2;

ALTER TABLE `dc_margin_option`
  ADD CONSTRAINT `dc_margin_option_ibfk_1` FOREIGN KEY (`default_kelas_margin_rajal`) REFERENCES `dc_kelas` (`id`) ON DELETE SET NULL ON UPDATE CASCADE;
```

tampilan menunya seperti apa

Adding Menu

```
INSERT INTO `dc_privileges` (`id`, `id_module`, `menu`, `url`, `icon`, `urutan`, `active`) 
VALUES (NULL, '4', 'Margin Obat', 'masterdata/margin_obat', 'fa fa-medkit', '0', '1');


INSERT INTO `dc_grant_privileges` (`id`, `id_group_users`, `id_privileges`) 
VALUES (NULL, '1', '255');
```


## Log
`07.27` datang
`08.14` learn Kotlin
`09.39` task 2
`14.34` rencana task 4
