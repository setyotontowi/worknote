---
tags: ['2020/[07] July']
title: '7 Jul, Tuesday'
created: '2020-07-07T01:29:21.502Z'
modified: '2020-07-15T11:53:48.738Z'
---

# 7 Jul, Tuesday

`Day 175` Ini tentang apa yang kau hasilkan, bukan apa yang kau tahu

- [x] 1. Pendaftaran Online: Bug: ketika difilter dan item diclick, maka indeksnya tidak sesuai. -> 6 Jul
- [x] 2. Pendaftaran Online: pekerjaan dan pendidikan diambil dari api
- [x] 3. Pendaftaran Online: Bug: next prev -> Task 1
- [x] 4. Pendaftaran Online: Kembali setelah pendaftaran baru
- [x] 5. Pendaftaran Online: Jika gagal, jelaskan kenapa dari errornya
- [x] 6. Pendaftaran Online: Bug, validasi wilayah yang belum diisi
- sepertinya provinsiAdapter, dsb tidak pernah digunakan.
- [x] 7. E-Doc: Setting Dokter
- [x] 8. E-Doc: Filter in General.
- [x] 9. E-Doc: App Setting, Dokternya masih belum terisi otomatis
- [x] 10. E-Doc: Buat Card Selamat Datang
- E-Doc: Settings. 

## Task 1
melanjutkan yang kemarin
- yang sebenernya terjadi adalah item yang diklik di eksekusi di luar adapter. lebih tepatnya di Dialog builder tersebut. 

## Task 6
kasih aja if else

## Note 1
tidak, itu digunakan untuk trigger onchange wilayah

## Note 2
- cek apa-apa saja settings yang diperlukan. Dokter, rotasi tablet. Dokter dipilih berdasarkan setting. Jika ada filter, maka yang didahulukan adalah filternya. 

## Task 7
mungkin karena dokternya kosong, jadi bisa muncul semua. Parameter apa yang dikirimkan oleh dokter tersebut? dia menggunakan id_dokter
- berarti mengubah POJO pasien menambahkan id_dokter. sepertinya tidak perlu karena tidak ada id dokter di setiap pasien. (`19.31`)
- simpan di sharedpreferences. sudah dicek (`19.34`)
- sewaktu awal load, dia akan ngecek apakah ada dokter yang disimpan di shared preferences (dari setting) jika ada maka ambil dari situ. jika tidak ada maka "". permasalahannya ada di arguments ketika dijalankan. 
- filter urusan nanti. tapi ini termasuk urusan filter juga. Dokter di filter harus di convert dari string ke dokter. edit text semuanya juga harus jalan `20.25` `expand to task 8`

## Task 8
- filter urusan nanti. tapi ini termasuk urusan filter juga. Dokter di filter harus di convert dari string ke dokter. edit text semuanya juga harus jalan, checked `20.57`
- pembuatan class Dokter dan Dokter Adapter implements filterable. however, semua yang menggunakan textwatcher belum bisa memilih dokter dengan baik. di app setting, masalah indexnya. di filter masalah id nya.
- dalam Pendaftaran online, aku pernah ingat ada fitur serupa, dia menggunakan onItemClick dan mengambil item dari adapter: lihat ke **Penelitian Lebih Lanjut** `21.19`
- buat Filterable untuk AppSetting terlebih dahulu. 

**Penelitian Lebih Lanjut**
- adapterView.getAdapter().getItem(i);
dia ambil dari situ. getAdapter kemungkinan mengambil Adapter (ProvinsiAdapter) yang telah di set. karena tidak mengimplementasikan filterable, maka kemungkinan bisa dijadikan satu dengan yang ada di AppSetting `21.20`


## Task 9
- Dokter dari sharedPreferences belum di masukkan ke AppSetting.

## Task 10
- Selamat Datang kembali dokter [Nama Dokter] 

## Logs
`07.03` init
`09.17` task 1 complete
`09.52` task 3 complete
`11.58` task 2 complete
`12.51` start
`13.59` task 4 complete
`14.27` task 5 complete
`14.37` task 6 complete
`19.00` Stage 2
`20.25` task 7 complete break (1 jam 25 menit)
`20.49` Stage 3
`20.53` task 9 complete
`21.24` break (35 menit) (total: 2 hours)
