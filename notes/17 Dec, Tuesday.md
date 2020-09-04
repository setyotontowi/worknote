---
tags: [2019/December]
title: '17 Dec, Tuesday'
created: '2019-12-17T00:28:37.190Z'
modified: '2019-12-17T08:30:00.364Z'
---

# 17 Dec, Tuesday

`Day 34`

- [ ] 1. SIMRS Temanggung : Log Masterdata
- [ ] 2. SIMRS Temanggung : check di live proses `<br>` 
- [ ] 3. SIMRS Dinda : masterdata baru

## Task 1

List Function (m_masterdata)
- Barang PF (Farmasi) : save_data_barang(), delete_data_barang()

## Task 3

tabel item laboratorium
dc_layanan, setiap layanan mengandung item laboratorium (dc_item_laboratorium)

ada nilai normal disitu, pembuatan master data nilai normal adalah untuk memilih di select option. hasil nilai normal diinputkan kemana. di dc_item_laboratorium hanya ada satu column nilai_normal

dc_nilai_normal_lab
: id, id_item_laboratorium, nilai_normal, kategori, operator, awal, akhir

jika ditambahkan di masterdata, apakah nanti akan berpengaruh di dc_nilai_normal_lab? yang mana bisa cuma hanya menggunakan grouping. 

jika memang ditambahkan berarti harus merubah tampilan menjadi nilai_normal_auto.

**keputusan**, pembuatan masterdata, berarti dc_nilai_normal_lab kemungkinan tidak akan terpakai.

```
CREATE TABLE `simrs_dinda`.`dc_kategori_nilai_normal` ( 
  `id` INT NOT NULL AUTO_INCREMENT , 
  `nama` VARCHAR(50) NOT NULL , 
  PRIMARY KEY (`id`)) ENGINE = InnoDB;
```

- [ ] Pembuatan Menu
- [ ] Pengaplikasian pada seluruh sistem
  - [ ] Masterdata -> Item laboratorium
  - [ ] Pelayanan -> Hasil laboratorium

ROLLBACK, yang diperlukan hanyalah kategori, tidak hanya laki-laki, perempuan atau anak.

## Log
`07.20` datang
`09.30` task 1
`10.30` end idle, start task 3
`13.13` salah pemahaman, bukan master data nilai normal. namun cuma kategorinya saja
`15.00` idle
`15.20` pulang
`15.30` keluar


## Random Notes

saat ini pekerjaanku hanyalah menambahkan masterdata baru di SIMRS Dinda dan mengecek kesalahan javascript yang ada di SIMRS Temanggung. Jam setengah sepuluh aku merasa tidak lagi semangat. Bukan berarti aku tidak mood untuk mengerjakan sesuatu, ada beberapa hal yang terpikirkan olehku, mengenai sumbangsih untuk perusahaan ini selama aku disini dan persiapanku untuk ke Jepang. 

sumbangsih dalam bentuk apa? 
bagaimana persiapanku untuk ke Jepang?

**Kekurangan apa yang dimiliki oleh perusahaan ini?**
1. Dokumentasi
2. Masih banyak bug minor setelah relase
3. Ketidakkonsistenan environment coding
4. Perlu waktu minimal satu jam hingga satu hari untuk menyelesaikan bug
5. Design android yang so-so
6. Jika menambah fitur baru, perlu ada penyesuaian dalam jumlah besar. contoh Margin Obat

**Pembaruan apa saja yang akan dilakukan oleh perusahaan ini?**
- Katanya ingin membuat aplikasi pendaftaran online untuk Seluruh Rumah Sakit 
- Usulanku, menambahkan fungsi pemanggilan ambulan. Atau bridging ke seluruh sistem rumah sakit

jika aku ingin meninggalkan kantor ini, aku ingin pekerjaan tidak bertambah susah dengan tanpa adanya diriku. berarti permasalahan mengenai kerangka bekerja?
