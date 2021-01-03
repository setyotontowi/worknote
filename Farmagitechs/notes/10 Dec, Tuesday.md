---
tags: [2019/December]
title: '10 Dec, Tuesday'
created: '2019-12-10T01:05:35.807Z'
modified: '2019-12-10T08:55:05.072Z'
---

# 10 Dec, Tuesday

`Day 30`

- [X] 1. SIMRS V2.0 Last Bug
- [ ] 2. SIMRS Temanggung : Perbaikan Nominal (Progress)
- [X] 3. Pendaftaran Online Siti Hajar
- [X] 4. SIMRS Temanggung : Edit Resep -> Blank
- [ ] 5. Deploy SIMRS v2.0 Ke Server.
- [X] 6. SIMRS Temanggung : Etiket Resep
- [X] 7. SIMRS Temanggung : Bug no R/ pada resep

## Task 1

- [ ] Hasil Laboratorium
Permasalahan :
> Ketika ditambahkan hasil laboratorium -> pemakaian BHP, data yang telah disimpan sebelumnya tidak muncul. ketika diinputkan obat lagi lalu klik tambah, data sebelumnya muncul bersamaan data yang telah ditambahkan tadi. Aku mengecek di database menggunakan query yang ada, memang tidak ada datanya. 

detail_pemeriksaan()
add_bhp() - get_bhp(id_lab) tombol tambah obat
#bt_tindakan tombol simpan tidak ada aksi yang mengirim ke server disana

get_bhp selalu return null juga dari dc_penjualan dan detailnya.
cek dimana add_bhp menyimpan
add_bhp to dc_detail_penjualan dan dc_penjualan

menggunakan query get_bhp(id_laboratorium) where id_lp = 813 datanya muncul, tapi id_laboratorium nya null. berarti permasalahan ketika save id_lab

Pilihannya ada 2
1. Menambahkan id_lab ketika menyimpan 
2. Menampilkan tanpa id_lab (chosen)

**Confirmed Done by Tester, Yet Hasn't Uploaded (Task 5)**

## Task 2
Pemesanan barang farmasi harganya berbeda dengan penerimaan barang.
data harga dari pemesanan barang harganya diambil darimana?
data harga dari penerimaan barang datanya diambil darimana

## Task 5
Deploy Server
ubah database add margin
 (PKU banjar, pku merden, pku purbalinggga) default layanan
push to repo.
update via updater to all

Update Database
- [ ] PKU Banjar
- [ ] PKU Merden
- [ ] PKU Purbalingga
- [X] RS Gunung Manik (local 100)


## Task 6
780610 id_resep
permasalahannya hanya di printing kemoterapi

## Log
`07.26` datang
`08.11` start doing task 1
`08.52` task 3 done, published to playstore
`09.31` task 1 done.
`09.43` task 4 done.
`11.00` break. did task 2 previously.
`12.37` start tark 5
`14.37` task 6-7 done
`15.56` pulang
