---
tags: [2019/December]
title: '6 Dec, Friday'
created: '2019-12-06T00:38:48.637Z'
modified: '2019-12-06T09:00:54.791Z'
---

# 6 Dec, Friday

`Day 28`

- [X] 1. SIMRS V2.0 Menu Implementation
  - [ ] Bug sewaktu tambah transaksi
- [X] 2. Android : Finishing : menunggu sertifikat
- [X] 3. SIMRS V2.0 masterdata : Setting Margin Option
- [ ] 4  Android Evoluzee demo

## Task 1

### Margin Kelas
Menu Yang Belum :

- [X] Resep rawat jalan (default kelas diambil dari database) **belum ditest(hitung)**
- [X] Resep rawat inap [status obat pulang]?
- [X] penjualan bebas **belum di test(hitung)**
- [X] pemeriksaan klinik **belum di test(hitung)** ada pop up data gagal dimuat
- [X] pemeriksaan IGD **belum di test(hitung)**
- [X] hasil laboratorium **belum di test** ada pop up data gagal dimuat
- [ ] hasil radiologi - tidak ada menunya
- [ ] pemeriksaan rawat inap - tidak ada menunya

**Knowledge**
seharusnya mengambil opsi_margin bisa dilakukan di auto barang (barang_with_stok_auto).
selanjutnya tinggal pengaturan kelas. 

tidak. jika dilakukan di barang_with_stok_auto akan melambatkan prosesnya karena perlu mengakses database 2 kali.

--

### Margin Range

- [X] Query
- [X] Implementasi ke menu

jika opsi diambil dari database, maka tidak ada perubahan pada menu-menu lainnya. di model akan dicek apakah opsi merupakan 'Range' atau 'Kelas' atau 'Layanan' yang mana diambil dari enum database.

### Bug
edit resep pasien rawat jalan atau rawat inap. ketika transaksi disimpan di database, harga jualnya jadi berubah.


## Task 2
Key Store Password : fgdefault
Key Password : fgdefault
Key Alias : key_fg

sepertinya memang harus menggunakan sertifikat yang sama.

## Log
`07.25` datang
`08.06` try coba publish android
`09.53` opsi margin kelas (menu implementation) done
`10.16` query margin range done
`10.24` menu implementation done
`14.52` tambah transaksi untuk semua menu
`15.50` discovered a bug
`16.02` pulang
