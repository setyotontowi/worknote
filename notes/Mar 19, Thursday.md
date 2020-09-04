---
tags: ['2020/[03] March']
title: 'Mar 19, Thursday'
created: '2020-03-18T21:11:28.346Z'
modified: '2020-03-19T07:00:49.744Z'
---

# Mar 19, Thursday

`Day 95`
`Day 50 Aceh`

- [X] Pendaftaran Online Dinda, RSMB: Penyesuaian Aplikasi dengan API
- [ ] E-Doc: Revisi 1: CodeReview
- [ ] E-Doc: SplashScreen Activity


## Task 1

1. Hide fitur **lupa password**
2. Booking menggunakan no RM langsung dari SharedPreferences
3. Hide menu **Tagihan**
4. Hide menu **Data Pasien Baru**
5. Hide menu **Ganti Password**

Langkah langkah
1. LoginFragment, layout. (this)
2. EntryOrder2Fragment. masukkan no RM langsung
3. Hilangkan Akses done
4. Hilangkan Akses done
5. Hilangkan Akses done

3-5 seharusnya selesai.
forgotpassword sudah di hide. tinggal proses login menggunakan RM dan Booking menggunakan RM. switch

### Issues
- logout masih belum bisa, dia menggunakan API. apakah mau diganti dengan menghapus sharedpreferences?
- Registrasi user masih belum jelas
- No RM ambil dari shared preferences
- SharedPreferences login belum diubah

---

Sesi 2
Login RM works
hash md5 in app. 
configure json
the rest is same.

Sesi 3
Tampilan, sepertinya di set manual di String, sama dengan assets-assets dan nama aplikasi. nama package?
keterangan: Logo dan Assets yang belum.

Sesi 4
No. 2 ? Menunggu backend.


## Task 2
Sesi 1
Terkait General Helper?
GeneralHelper tidak mengandung volley sama sekali. tetapi seperti pengkonstruksian header.
Menggunakan volley callback
[callback](https://stackoverflow.com/questions/40948598/android-volley-return-value-from-response?noredirect=1&lq=1)
[callback main](https://stackoverflow.com/questions/28120029)

sesi 5
general helper.

## Log
`04.59` start working
`06.39` forgotpassword sudah di hide...
`09.28` starting task 1
`10.44` sesi 3 selesai dengan keterangan.
`11.16` idle.
`13.00` start working task 2

