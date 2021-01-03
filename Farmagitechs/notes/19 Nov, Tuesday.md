---
attachments: [signup-login5.zip]
tags: [2019/November]
title: '19 Nov, Tuesday'
created: '2019-11-19T02:35:03.279Z'
modified: '2019-11-22T06:53:36.649Z'
---

# 19 Nov, Tuesday

`Day 15`

- [X] Debugging Android
- [ ] Android Documentation
- [ ] Laporan Online SIM RS Dinda

## Task 1
untuk menambahkan about atau tentang, aku harus mengubah layout di AccountFragment. pada awalnya, layout yang digunakan hanyalah RecylerView. diperlukan sisipan view dari about view dan wadah untuk menggabungkan keduanya. 

kemudian untuk menambahkan dan mengedit tampilan link juga tidak semudah html. link diedit dalam java menggunakan Class baru dan Spannable Class

## Task 2
seperti yang telah dijelaskan sebelumnya, membuat laporan online menggunakan database. setiap session yang dibuat, akan merubah status menjadi online atau offline. permasalahannya adalah ketika session destroy secara otomatis.

di [code](@attachments/signup-login5.zip) dijelaskan untuk bisa mengupdate status logout ketika user tidak aktif maka diperlukan timer yang perlu dipanggil di seluruh file. 

bagaimana jika berbentuk log? 
setiap fungsi update_log() yang dipanggil ketika session dibuat, maka harus ngecek data terakhir apa, jika masih online, maka akan diupdate saat itu juga.

mungkin sekitar 1-2 hari.
1. Log Add Login
    1. Add table
    2. Try login button
2. Setelah beberapa data, toggle status.
3. Set Session
```
Skenario 1 Logout Otomatis
user A, B, C
hari login


A login 1
B login 1
C tidak login

B logout otomatis, sehingga di sistem 1
C login 1

Maka A, B, C login 1
padahal ada hanya ada A, C
bisakah melihat session yang aktif?
```

```
Skenario 2 Log perlu di update atau tidak?

A login 07.00, logout 12.00
A login 18.00, logout - 

menambah log baru atau mengupdate yang telah ada?
```

bentuk laporannya adalah siapa yang login sekarang. yang terpenting adalah waktu login. jam berapa aja dia login?
siapa aja yang login di hari ini? besar kemungkinan dia menekan tombol logout karena shift berganti. sehingga skenario 1 bisa diabaikan

> percobaan accomplished
> langsung ke sistem

ketika di update, dan tidak ada tabel maka yang terjadi adalah error. maka sebelum push, sebaiknya konfirmasi terlebih dahulu

### What do I need?
1. tabel dc_session(id, user, waktu login, waktu logout) done
2. informasi relasi user : tabel user
3. Menu sistem [controller/sistem]
4. fungsi di login sistem [controller/users]
5. fungsi untuk memfilter, nama - hari dari sampai [m_users] di eksekusi di users di logmein
6. [controller/users/logout]

```
CREATE TABLE dc_session (
  id INT(11) AUTO INCREMENT PRIMARY KEY,
  id_user INT(11),
  id_unit INT (11),
  id_jabatan INT (11),
  login DATETIME,
  logout DATETIME
);

ALTER TABLE `dc_session` ADD 
CONSTRAINT `dc_session_ibfk_1` 
FOREIGN KEY (`id_user`) REFERENCES `dc_users`(`id`) 
ON DELETE RESTRICT 
ON UPDATE RESTRICT;

ALTER TABLE `dc_session` ADD 
CONSTRAINT `dc_session_ibfk_2` 
FOREIGN KEY (`id_unit`) REFERENCES `dc_unit`(`id`) 
ON DELETE RESTRICT 
ON UPDATE RESTRICT;

ALTER TABLE `dc_session` ADD 
CONSTRAINT `dc_session_ibfk_3` 
FOREIGN KEY (`id_jabatan`) REFERENCES `dc_jabatan`(`id`) 
ON DELETE RESTRICT 
ON UPDATE RESTRICT;
```

## Log
`09.34` Menambahkan about
`10.19` Laporan Online SIM RS (Percobaan)
`13.46` Menyusun rencana untuk membangun aplikasi
`15.51` insert ke database : done
