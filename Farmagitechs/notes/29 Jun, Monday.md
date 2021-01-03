---
tags: ['2020/[06] June']
title: '29 Jun, Monday'
created: '2020-06-29T00:57:26.176Z'
modified: '2020-07-04T01:55:55.711Z'
---

# 29 Jun, Monday

`Day 169` Lanjutan Sabtu

- [x] SIMRS Report: Export Kunjungan Laboratorium dan Kunjungan Radiologi: BX0wVWrG: 
- [x] SIMRS V2: Tambahan Nilai Normal Terdeteksi IYGKexiH
- [x] SIMRS Report: Dokter Radiologi -> Task 1
- [x] E-Doc: Revisi 3: Dismiss Dialog Dokumen: XpIRw0zp
- [x] SIMRS Report: Push To Live -> Task 1

Kerjakan task 2 terlebih dahulu baru task 1. karena kelihatannya task 2 lebih mudah untuk dikerjakan

## Task 1
Tentang kemarin
Untuk kunjungan radiologi, tampaknya aku telah menambahkan dokter disana. dokter pengirim merupakan dokter dari poli dimana dia berasal. sedangkan dokter radiografer adalah dokter yang melakukan radiografi. permasalahannya adalah dokter radiografi tidak serta merta satu dokter yang melakukan tugas di item radiologi. kadang ada dokter yang berbeda per item radiologi. Sedangkan yang ditampilkan di report hanya satu dokter radiologi.

**Current Status**
- [x] Kunjungan Radiologi, Dokter Pengirim
- [x] Kunjungan Radiologi, Dokter Radiologi Expand to Task 3 (tidak diperlukan)
- [x] Kunjungan Laboratorium, Dokter Pengirim

**Complete**
Task 1.1: mengubah query di mRadiologi.scala
Task 1.3: mengubah queri di mLaboratory, mengubah param kunjunganLaboratorium di mLaboratory, alhasil mengubah juga format method yang digunakan di lain file termasuk mJasaMedisPenunjang dan di Laboratory

**Finish**
- commit message.
- push to repo, all simrs v2 using ssh.


## Task 2
**From 15 Jun**
- Abnormal di hasil lab. finish, in 3 view: `hasil_laboratorium`, `laboratorium_form2`, `laboratorium_langsung`.
- Rule Reaktif - Non Reaktif. finish in `m_masterdata/get_operator`
- penambahan enum di database table: `dc_nilai_normal_lab` col operator. finish

```sql
ALTER TABLE `dc_nilai_normal_lab` 
CHANGE `operator` `operator` 
ENUM('-','<','<=','>','>=','Positif','Negatif','Reaktif','Non Reaktif','Tertedeksi','Tidak Terdeteksi') 
CHARACTER SET latin1 COLLATE latin1_swedish_ci NOT NULL;
```

**Notes**
- penambahan enum di semua database terkait versi 2 di mas joko, also localhost (fin)

## Task 4
**Intermezzo**
Terkait edoc, riwayat dokumen tetap pada desain original. sedangkan ada tambahan krusial mengenai dokumen pasien (seperti KTP atau riwayat kunjungan dsb) di dalam card pasien. tetap saja, setelah ini aku harus mengerjakan terlebih dahulu bug nya, lalu mengembangkan fitur dan halaman terbaru.

**Problem**

## Task 5
**Push to live**
- Upload to repo (fin)
- Update to live


**How to Upload File**
- sbt stage (for first use) / sbt dist (for next)
- locate in target/universal/stage/lib
- Using Filezilla, connect as usual
- Restart app using sudo /etc/init.d/reportv2 stop|start


## Logs
`07.08` init
`08.29` task 2 selesai
`09.56` task 1 selesai
`10.52` terkait edoc
`15.02` update live done

## Epilogue
- Text Extraction
