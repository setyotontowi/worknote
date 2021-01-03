---
tags: [2019/November]
title: '20 Nov, Wednesday'
created: '2019-11-20T00:55:59.351Z'
modified: '2019-11-21T04:28:50.950Z'
---

# 20 Nov, Wednesday

`Day 16`

- [X] RS Dinda Laporan Login
    - [X] Revisi menambahkan id_unit dan id_jabatan. selain itu cek sessionnya di app.php index()
- [ ] Android Documentation
- [ ] Dokumen High Alert Medication diberi judul dan dibuat center

## Task 1
1. Membuat menu
    1. controllers/sistem membuat fungsi baru untuk menunya
    2. update database tentang menu barunya.
    3. create view
    4. create models at first m_sistem lewat api/sistem
    5. tampilan tabel adalah 
        | No  | Nama | Unit | Jabatan | User Grup | Waktu Login | Waktu Logout | Status |
        |-----|------|------|---------|-----------|-------------|--------------|--------|


2. Membuat laporan
    1. Filter hari dan user
3. Testing

### Quick Notes
- menambahkan kolom ip untuk skenario satu user login di beda komputer. step selanjutnya
- menambahkan menu : dc_module, dc_privileges
  - insert to dc_privileges
  - grant to dc_grant_privileges
- menambahkan status login
- `12.01` ip di database, ip di module, filter tanggal query, username_auto, EXPORT
- where ip. jika sesi sebelumnya belum logout

```
select a.*, b.username, c.nama as unit, d.nama as group_user, e.nama as nama_lengkap
                FROM `dc_session` a 
                JOIN dc_users b on a.id_user = b.id
                JOIN dc_unit c on b.id_unit = c.id
                JOIN dc_group_users d on b.id_group_users = d.id
                JOIN dc_pegawai e on a.id_user = e.id
				LEFT JOIN dc_jabatan f on e.id_jabatan = f.id
```

**Menu**

```
SELECT a.*, e.nama as module, d.menu, b.nama, c.username FROM `dc_grant_privileges` a 
JOIN dc_group_users b on a.id_group_users = b.id
JOIN dc_users c on b.id = c.id_group_users 
JOIN dc_privileges d on d.id = a.id_privileges
JOIN dc_module e on d.id_module = e.id
WHERE c.username = 'joko'
```


## Log
`07.33` Datang
`08.11` Start working on task 1
`09.34` Model done
`09.47` Controller/api done. now making view
`10.17` progress on adding menu
`10.25` menu ditambahkan
`10.49` tabel tampil
`11.15` ip bisa tampil tapi belum masuk ke database
`12.14` ip masuk ke database
`12.58` filter tanggal selesai
`13.28` view selesai
`14.13` printing excel selesai
