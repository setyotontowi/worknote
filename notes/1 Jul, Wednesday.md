---
tags: ['2020/[07] July']
title: '1 Jul, Wednesday'
created: '2020-07-01T00:18:23.743Z'
modified: '2020-07-05T09:13:13.894Z'
---

# 1 Jul, Wednesday

`Day 171` Patuh dan Taat

- [x] 1. E-Doc: Revisi 3: Penambahan Label pada cards pasien adHiBdfn -> 30 Jun
- [x] 2. E-Doc: Revisi 3: Add logout button e9T80HcS -> 30 Jun
- [x] 3. E-Doc: Revisi 3: Splash Screen belum berfungsi
- [x] 4. E-Doc: Progress dialog -> Task 3
- [x] 5. E-Doc: Loginnya terlalu besar dan tidak sesuai tinggi keyboard
- [x] 6. E-Doc: Konfigurasi kembali model Pasien.class -> Task 1
- [x] 7. E-Doc: List yang dipilih, warnanya menjadi gelap.
- Migration to Butterknife, nope ViewBinding

## Task 1
**Note**
- Tambahan Atribute: Tanggal Kunjungan, Dokter, Layanan
- Redesign Tampilan Kartu

**Ganti Icon**
1. Tanggal Lahir diganti dengan icon bayi
2. icon tanggal dibuat untuk tanggal kunjungan
3. terdiri dari dua panel, kanan dan kiri. kiri untuk data kunjungan, kanan untuk data pasien
4. data kunjungan terdiri dari tanggal kunjungan, dokter dan poli, sedangkan kanan data pasien terdiri dari No RM, Tanggal Lahir, jenis kelamin/no registrasi
5. icon rm dibuat sendiri dengan RM dikasih box

## Task 3
**Note**
somehow, callbacknya lama dibandingkan dengan eksekusinya. https://stackoverflow.com/questions/6847697/how-to-return-value-from-an-asynchronous-callback-function

**Furthermore**
kasih dialog di splash screennya

## Task 5 
**Complete**
- dengan next/prev key event

## Task 6
sepertinya data mengenai pasien (POJO) masih ada yang belum sesuai

## Logs
`07.07` init
`09.10` task 3 done
`09.26` task 4 done
`09.58` task 2 done
`13.59` task 1 done
`14.09` start implementing butterknife
`10.03` task 5 complete
`19.28` sesi 2 start
`20.15` sesi 2 complete (1 Jam)
