---
tags: ['2020/[08] August']
title: '10 Aug, Monday'
created: '2020-08-10T00:49:18.291Z'
modified: '2020-08-11T06:29:22.745Z'
---

# 10 Aug, Monday

`Day 199` Embrace it

- [x] Pendaftaran Online: Apps Suspended
- [x] Edoc: Kamera

## Task 1
- test app pake alamat ip baru.
- pelajari apa yang menyebabkan aplikasi tidak diterima.

Kecurigaan:
1. Unable to publish similar app and name [Link](https://www.quora.com/Is-there-anything-in-Google-Play-s-policy-that-prevents-you-from-publishing-2-similar-apps-that-use-the-partial-common-codes-The-UI-is-different-but-the-engine-of-both-apps-is-similar)
2. Unless they are changes in these: Package Name, App Name, Icon, Screenshot App [Link](https://www.quora.com/May-I-upload-an-APK-already-on-the-Play-Store-to-the-Play-Store-after-changing-its-package-name-icon-and-app-name)

Dari kedua hal di atas, ada kemungkinan app suspended karena screenshot app yang serupa. atau (belum mengecek) keystore yang sama dengan sebelumnya (rsudtmg)

Namun:
Aplikasi yang kita ajukan melanggar Deceptive Privacy Policy. yang mana jauh sekali dari apa yang kita tangkap. Aku telah mengajukan review ulang terkait ini. Namun dengan ada Impersonation Policy, perlu dipertimbangkan perilisan aplikasi evoluzee untuk rumah sakit yang lainnya.  

Topic:
Impersonation Policy. Antara RSMB dan PKU Purbalingga. Berbeda Developer Name, namun aplikasi, nama, icon dan lain sebagainya persis serupa. Sebenarnya bisa jika kita mencoba mengupload Evoluzee RSU PBG, namun ada kemungkinan melanggar policy tersebut

## Task 2
Start 10.12
- [x] First Item in Adapter
- [x] OnClick Open Camera
- [x] OnActivityResult

Problem:
dalam membuka kamera tidak bisa dilakukan adapter. dia harus berada di dalam activity. apa perlu menggunakan callback?

Break 10.49 - 10.55
tinggal di jalankan-test (11.37)

`13.20` Problem: data yang dikirim dari kamera null.
`14.04` java.io.FileNotFoundException: open failed: EACCES (Permission denied)

## Logs
`07.23` init
`09.54` pengajuan banding
`13.05` membuka kamera, namun masih error

