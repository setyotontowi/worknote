---
tags: [2019/December]
title: '16 Dec, Monday'
created: '2019-12-16T01:18:35.722Z'
modified: '2019-12-16T08:41:01.785Z'
---

# 16 Dec, Monday

`Day 33`

- [ ] 1. SIMRS Dinda : masterdata baru
- [ ] 2. SIMRS Temanggung : log masterdata 
- [X] 3. Checking Android

## Task 1

## Task 2

- [ ] Transaksi
- [ ] Menu

Pembuatan masterdata ICD X & 0

pada dasarnya log untuk masterdata sudah ditampung oleh sistem log. hanya saja sistem log hanya menampilkan yang error saja. tidak semua transaksi.

berarti jika satu table, log untuk masterdata juga ditampilkan. bagaimana caranya agar bisa memisahkan log untuk masterdata? berbeda tabel? 
keputusan : **berbeda tabel**

```
CREATE TABLE `dc_log_masterdata` ( 
`id` INT NOT NULL AUTO_INCREMENT , 
`menu` VARCHAR(40) NOT NULL , 
`waktu` VARCHAR(50) NOT NULL , 
`status` INT NULL , 
`url` VARCHAR(100) NOT NULL,
`response` TEXT NULL , 
`id_user` INT NOT NULL , 
PRIMARY KEY (`id`)) 

ALTER TABLE `dc_log_masterdata` 
ADD  CONSTRAINT `dc_log_masterdata_ibfk_1` 
FOREIGN KEY (`id_user`) 
REFERENCES `dc_users`(`id`) ON DELETE RESTRICT ON UPDATE RESTRICT;

```
ajaxSuccess adalah recursive. ketika dia memasukkan log_masterdata, dan itu sukses, itu akan memanggil ajaxSuccess.

kembali ke struktur data, aku ingin apa yang di ubah, dan data apa saja yang dikirimkan

rollback, ternyata database sudah ada. yang belum tinggal menambahkan log di setiap transaksi dan benerin di lokalnya. 

- [ ] benerin sistem masterdata di lokal
- [ ] tambah di model

List Function (m_masterdata)
- ICD X : update_data_golongan_sebab, delete_data_golongan_sebab `done`
- Gizi : save_data_barang_no, delete_data_barang

## Random Notes
- Gizi, belum ada json kemasan barang.

## Log
`07.54` Datang
`08.00` checking android
`10.05` task 2 progress

## Random Notes
- kekuranganku adalah ketelitian
