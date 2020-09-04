---
tags: [2019/December]
title: '5 Dec, Thursday'
created: '2019-12-05T00:27:22.565Z'
modified: '2019-12-06T01:21:07.115Z'
---

# 5 Dec, Thursday

`Day 27`

- [ ] 1. SIMRS V2.0 Implementasi ke menu
- [X] 2. Pendaftara Online Siti Hajar Android Bug

## Task 1

- [X] Generating query
- [X] controllers resep rawat jalan, pass data dc_margin_option.id
      get option id di controller view atau di model? di controller view
- [X] rawat inap

      tambahan kelas tempat pasien dirawat
      `m_pelayanan/get_list_layanan_pendaftaran_tindakan_bhp` untuk get list pasien
      `m_pelayanan/get_layanan_pendaftaran` untuk entry resep ranap

      relasi kedua tabel di atas sudah sama. ada kemungkinan memang ada data yang tidak lengkap
      kurang testing kepastian perhitungan harga

- [ ] penjualan bebas
- [ ] pemeriksaan klinik
- [ ] pemeriksaan IGD
- [ ] hasil laboratorium
- [ ] hasil radiologi
- [ ] pemeriksaan rawat inap

yang dibutuhkan id atau default kelas rawat jalan?
enum kelas, layanan, atau range

pembagian rawat jalan dan rawat inap per menu. setiap menu rawat jalan akan dikasih hidden input default_kelas_rawat_jalan

kalau optionnya layanan seperti biasanya
kalau optionnya kelas dibagi menjadi 2 rawat jalan (default) dan rawat inap (butuh parameter kelas)
bagaimana dengan unit penunjang? unit penunjang bisa dari rawat jalan dan rawat inap. berarti harus ngecek satu satu menunya. tidak bisa jika tidak.

**tinggal menyesuaikan menu lainnya**
ditambahi di controller waktu ngeload ambil margin_option

> **CATATAN**
```
kelas diambil dari pasien rawat inap, jika tidak ada kelas di data pasien maka diambil dari default dari rawat jalan, jika tidak ada pasien terdata di pendaftaran maka tetap diambil dari default rawat jalan

```

### File
m_masterdata/get_auto_barang_stok     

## Task 2
username:"latiev","password":"123456"

{"pk_poliklinik":"16","tgl_daftar":"2019-12-05"}

## Log
`07.27` datang
`08.41` Start Task 1
`09.29` query done
`09.49` switch to android
`13.31` rawat jalan done
`16.15` pulang
