---
tags: ['2020/[06] June']
title: '15 Jun, Monday'
created: '2020-06-15T00:58:03.903Z'
modified: '2020-06-15T08:00:31.995Z'
---

# 15 Jun, Monday

`Day 159` 

- [x] Pendaftaran Online: Persiapan presentasi oleh RS Mentari Tangerang
- [ ] E-Doc: Side Quest: Redesign: Parent -> 10 Jun

## Task 1
**Note**
- setup mysql
- setup postgres
- RM "107975" KTP "1871010907930009"

**Problems**
- Error gagal daftar terkait cara bayar -> error terkait bridging to simrs. `10.11` error terkait return value dari simrs. `10.53` error constraint dc_users, solusinya menambahkan id = 3 yang mana menurut databasenya mas joko merupakan user khusus pendaftaran online.

## Task 2 
Main Fragment

**Todo**
- https://github.com/ToDou/CalendarPager using this as a filter date, or https://github.com/Mulham-Raee/Horizontal-Calendar 

**Note**
- SimplePagerAdapter mPagerAdapter.
- WeekRecylcerView in WeekPagerActivity
- WeekDayViewPager mViewPagerContent
- Library ini diharuskan untuk membuat ViewPager untuk contentnya agar bisa swipe right/left. berarti nanti dibungkus fragment kembali. Main Fragment{ WeekRecyclerView as sliding calendar, WeekDayViewPager as Content Slider {PasienList, Pasien} }

## Logs
`07.29` init
`08.12` Session 1: Task 1: Gathering Information and Trial
`08.42` Session 2: Task 1: Try on tablet
`09.12` Session 3: Task 1: Debug terkait gagal daftar
`09.42` Session 4: Task 1: Json Array in Backend: Finding out
`10.12` Session 5: Task 1: Check API SIMRS:
`10.42` Session 6: Task 1: Finished 
`11.12` Interlude.
`13.00` Session 7: Task 2: Implementasi CalendarPager
`13.30` Session 8: Task 2: Pelajari todou CalendarPager
`14.00` Session 9: Task 2: Pelajari todou CalendarPager
`14.30` Session 10: Task 2: Pelajari todou CalendarPager
