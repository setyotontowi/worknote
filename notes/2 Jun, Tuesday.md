---
tags: ['2020/[06] June']
title: '2 Jun, Tuesday'
created: '2020-06-01T23:53:43.916Z'
modified: '2020-07-01T04:50:11.380Z'
---

# 2 Jun, Tuesday

`Day 150` Strategi percepatan

- [x] SIMRS V2: Operasi IGD /c/ahE4r6Dy/
- [ ] SIMRS V2: Penyesuaian Nilai Normal Lab IaWflCWJ
- [x] SIMRS V2: Validasi entri pemeriksaan lab pada pasien batal kunjungan n2AoTkX2 (Belum Push)
- [x] SIMRS V2: Lokasi Surat Keterangan Sakit dibuat dinamis 7S6MTz08

## Task 1
Research Conducted
Previous Note
e: semua database live untuk dc_tarif_operasi memiliki 14 kolom. tapi codingnya memerlukan 19 kolom.
e: semua database live versi 1 dc_tarif_operasi memiliki 26 kolom.

**Finished**
Case cancelled

## Task 2
Masterdata -> Nilai Normal

**Note**
- barusan aku cek, di master data nilai normal, aku entry angka 7,5. tp di hasil lab dan cetak hasil tetep munculnya 7,50 - zai

- it looks like it gonna take long.

## Task 3

**Todo**
Kunjungan pasien ke poli. Batalkan. Cek entri lab

**Finished**
aku tampilkan column status di query (m_penunjang/get_list_layanan_pendaftaran) lalu di viewsnya (get_list_pasien()) terdapat validasi dimana pasien lunas atau pasien batal (v.lunas !== Belum OR v.status == Batal)

## Task 4
cek masterdata lokasi. 
dari dc_kelurahan, kecamatan, lalu kabupaten. diambil dari situ.

**Todo**
- pull from repo for update

**Finished**
ketika mengecek dokumen, ternyata lokasi sudah sesuai dengan kabupatennya.


## Logs
`06.53` start
`08.01` task 2 finished
`09.31` task 1 finished
`09.57` task 3 finished
`12.56` task 4 finished
