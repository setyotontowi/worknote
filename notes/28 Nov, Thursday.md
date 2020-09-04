---
tags: [2019/November]
title: '28 Nov, Thursday'
created: '2019-11-28T03:28:48.510Z'
modified: '2019-11-28T07:26:25.439Z'
---

# 28 Nov, Thursday

`Day 22`

- [X] 1. SIMRS Dinda : Layanan di Rekap Billing tidak muncul
- [X] 2. SIMRS Dinda : Tampilan Status Bed
- [X] 3. SIMRS Temanggung : Etiket dua nama
- [ ] 4. SIMRS Dinda : Log Login masih belum muncul

## Task 1
Latar Belakang
dijelaskan oleh mba putri bahwa kolom layanan yang ada di rekap billing berasal dari unit tempat pendaftaran/ layanan atau layanan penunjang. masuk di dc_pendaftaran kolom keterangan. 

berarti harus mengecek alur pendaftaran layanan penunjang. karena disitu tidak masuk ke dc_pendaftaran keterangan.

**Files** Menu Rekap Billing
1. `views/keuangan/billing/rekap_billing.php`
2. `controllers/keuangan.php`
3. `controllers/api/keuangan.php`
4. `models/m_keuangan.php`

**Query** List Rekap Billing
```
select pd.*, p.nama, lp.jenis, 0 as saldo_deposit, p.kelamin, p.alamat, lp.cara_bayar, IFNULL(pj.nama, '') as penjamin, IFNULL(pj.diskon, 0) as diskon_asuransi,
IFNULL(sp.nama, '') as spesialisasi, pd.lunas,
if(lp.ikw = 'Ya', 'VIP', '') as vip, '' as trx, 
pg.id as id_dokter, IFNULL(pg.nama, '') as dokter, pd.keterangan, pd.status as status_billing 

from dc_pendaftaran pd 
join dc_pasien p on (pd.id_pasien = p.id) 
left join dc_layanan_pendaftaran lp on (pd.id = lp.id_pendaftaran) 
left join dc_spesialisasi sp on (sp.id = lp.id_unit_layanan)
left join dc_penjamin pj on (pj.id = lp.id_penjamin) 
left join dc_nakes nk on (lp.id_dokter = nk.id) 
left join dc_pegawai pg on (nk.id_pegawai = pg.id) 

where pd.id is not null
and id_pasien = 107270
or id_pasien = 107731
group by pd.id
```

Problems.
karena keterangan di layanan penunjang hemodialisa tidak ada, maka memang tidak masuk di dc_pendaftaran kolom keterangan juga tidak ada.
proof : coba di pelayanan rm
edit : sampe sekarang aku belum nemu dimana waktu ngisi kolom keterangan

## Task 2

**checklist**
Filename: models/m_pelayanan.php
Line Number: 6802

**files**
1. `models/m_pelayanan/get_available_bed`
2. `controllers/laporan_pelayanan/list_status_bed`
3. `views/laporan/pelayanan/list_status_bed`
4. `controllers/api/pelayanan/get_available_bed_get`

## Log

`09.56` datang
`10.30` task 1
`12.33` task 1 done
`13.36` task 2 done (don't forget to remove (array))
`13.42` **notice** task 3 tgl 27 belum di push
`13.44` **notice** task 2 belum di push sizeof sudah dihilangkan
`13.52` revisi task 1 done
`14.03` updated to live : 2 today's task and 1(task 3) yesterday
`14.18` task 3 done. updated to live.


