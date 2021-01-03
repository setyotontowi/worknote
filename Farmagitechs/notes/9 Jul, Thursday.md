---
tags: ['2020/[07] July']
title: '9 Jul, Thursday'
created: '2020-07-09T00:40:19.029Z'
modified: '2020-07-15T02:35:50.108Z'
---

# 9 Jul, Thursday

`Day 177` Dengan secangkir kopi

- [x] 1. E-Doc: Filter in General -> July 7 
- [x] 2. Pendaftaran Online: Implementasi KTP
- E-Doc Context: Filter
- [x] 3. E-Doc: Bug 1: CalendarPager
- [x] 4. E-Doc: Improvement 1: AutoCompleteTextView
- [x] 5. E-Doc: Improvement 2: CalendarPager
- [x] 6. E-Doc: Improvement 3: AutoCompleteTextView
- [x] 7. E-Doc: Bug 2: ListPasienFragment, masih terkait filter

Take Online Registration first and primary priority. It'll be implemented on next week. While we made mistake not going extra work yesterday, It still can be manageable. 

## Task 1


## Task 2
Multipart copy from url.

## Task 3
- (problem) ketika filter dijalankan bersamaan dengan tanggal, calendarpager menampilkan sehari setelahnya meskipun datanya benar

## Task 4
- (improvement) tampilan autocompleteTextView

## Task 5
- (improvement) Tanggal di seluruh Aplikasi di set di Filternya. seperti dokter.
- (complete) sepertinya ini tidak diperlukan. karena masih menunggu konfirmasi dari behaviour user.

## Task 6
- (improvement) ketika item di filter telah di klik, dia tetap menampilkan kembali list dokternya.

## Task 7
- (bug) mengapa listPasienFragment berjalan dua kali?
- (complete partially) ada dua keadaan dimana ini terjadi. pertama ketika pertama kalinya (ini masalahnya ada di xml yang menggunakan fragment daripada Framelayout) dan ketika filter.
- (finding) bundle yang diambil adalah bundle yang dari main fragment meskipun filter telah dieksekusi. atau itu adalah residu dari main fragment saat load di awalnya sedangkan yang dari filter tidak bisa diteruskan bundlenya. 
- (finding) Jadi memang ada dua. ketika Filter dijalankan, CalendarPager berubah, berarti argumennya (bundle) juga ikut disitu. Sedangkan di Filter juga dibuat kembali. 
- (todo) Jadi, dibuat if else saja di CalendarPager selectedDatenya di MainFragment. if argument tidak ada maka buat baru, jika ada pake itu.


## Logs
`07.00` init
`18.42` stage 2 percobaan filter
`20.35` task 1, task 6
`20.57` task 3 complete
`21.41` task 5 complete
`23.27` finished (4 Jam 45 menit)


