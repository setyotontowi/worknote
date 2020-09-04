---
tags: ['2020/[06] June']
title: '26 Jun, Friday'
created: '2020-06-26T00:22:07.750Z'
modified: '2020-06-26T14:48:26.425Z'
---

# 26 Jun, Friday

`Day 167` More Analysis

For edoc. I will review my code first, cleaning up whilst recalling the code structure, package etc. Then, I will debug on list 3 and 3.1. Finally, I will do the fourth stage development

- [x] E-Doc: Code Review
- [x] E-Doc: Revisi 3.1 Problem 2 -> 17 Jun
- [x] E-Doc: Minor Bug #6:
- [x] E-Doc: Revisi 3.3: Terkait Filter including Revisi 3.1 Problem 3;
- [x] E-Doc: Revisi 3.3: Problem 2 -> Task 4
- [x] E-Doc: Revisi 3.3: CalendarPager mengikuti tampilan

- Hereby,  Revisi 3.1, 3.2, 3.3 All done

## Task 1
**Note**
- sampai saat ini, masih ada yang error terkait dengan pemilihan pasiennya. kemungkinan karena adanya perubahan terkait filter tersebut. 
- cleaning unused code

**On Hold**
1. Checking The files

## Task 2
- DocumentType List, using id as doc type [NTGp3O1X]

ini juga yang termasuk yang ditanyakan zai sewaktu presentasi kemarin. tentang tipe dokumen yang statis. 

**Todo**
- (IN) PasienFragment dialogForm()
- Get Tipe Dokumen from API
- Send it in createDoc()

**Todo More**
- Create Class Document
- Assign result from volley to document

**Note**
- dialogForm()
- createDoc()
- getDocumentType() assigntoclass

**Finished**
belum dengan nama karena tampilan juga akan dirombak.

## Task 3
Pasien yang ada dokumennya ketika di klik result error. kemungkinan terkait inflating ke PasienFragment

**Finished**
Ada tipo di layoutnya

## Task 4
**Problem**
- Semua tombol tidak bisa berfungsi, termasuk spinner. (fin)
- Revisi 3.1 Problem 3 -> 17 Jun : Revisi: Manggil melalui fragment onClick Hide this.
- Setelah tampilkan, maka calendarPagernya juga berubah inherit to task 6

**Problem 1**
- karena filter layout sama sekali belum diinsiasi, maka tidak akan ada aksi. karena layoutnya pun cuma sebatas include (fin)

**Problem 2**
- Cara manggil antar fragment begimane? try to call using instance as in FilterFragment. inherited to task 5

## Task 5
- Ada MainFragment dan FilterFragment. FilterFrag-

**Finished**
- call by using getParentFragment()

## Task 6
**Finished**
using horizontalCalendar.setRange and refresh

## Logs
`07.07` init
`09.07` Session 1: Task 2: Planning
`09.33` Session 2: Task 2: Implementation
`10.08` Session 3: Task 2: Display dialog, Task 3
`18.56` The Post Work
`20.54` Bingung masalah interface.
`20.58` Task 4 and 5 finished
`21.23` Task 6 finished

## Post Work
- Pelajari Fragment Manager
- terkait dengan permasalahan task 4 problem 2, bisa menggunakan view model atau (mungkin) bisa juga menggunakan [interface](https://developer.android.com/training/basics/fragments/communicating): use interface
- interface adalah hal yang perlu diimplementasikan di suatu class. misalkan Animal haveSound(). maka class pig implement haveSound() akan membuat method dimana Pig mempunyai sound "woo";
- `20.58` finished
- for redesign, list https://id.pinterest.com/pin/862439397378045986/
- jumlah kunjungan pasien dan dashboard
