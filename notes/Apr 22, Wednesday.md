---
tags: ['2020/[04] April']
title: 'Apr 22, Wednesday'
created: '2020-04-21T23:34:51.398Z'
modified: '2020-04-27T03:36:16.663Z'
---

# Apr 22, Wednesday

`Day 119`

- [ ] SIMRS V2: Hasil Lab: Perbaikan tampilan cetak hasil lab

## Task 1
permasalahan belum ketemu. coba lihat trello lagi dan perhatikan baik-baik.
ambil contoh 
- item lab ACA IG, setiap kelas berbeda-beda. 
- RESA Q, kelas III ranap

setelah di cek kembali, keyword kelasnya tetap ga muncul. 

Update 10.44
permasalahannya ada di komponen tarif. sepenuhnya di atur oleh mba putri. kemudian mba putri ngecek di entri lab lalu menemukan error bahwa semua item lab tidak muncul. padahal ketika aku input dari menu pelayanan ranap, item labnya muncul. itu (hipotesis) disebabkan karena ada satu parameter Kelas yang ikut terfilter.

sql dari masterdata_auto komponen_tarif_auto

```sql
select kt.*, jp.nama as jenis_pemeriksaan, 
IFNULL(kt.jenis, '') as jenis, 
IFNULL(b.nama, '') as bobot,
if(ll.nama is not null, 
   concat_ws(', ', l.nama, concat_ws('','<i>',ll.nama,'</i>'), kt.keterangan), 
   concat_ws(', ', l.nama, kt.keterangan)) as layanan, 'nonkelas' as kelas,
IFNULL(u.nama,'<i>Semua Instalasi</i>') as unit , IFNULL(k.nama,'-') as kelas 

from dc_komponen_tarif kt
left join dc_kelas_komponen_tarif kkt on (kkt.id_komponen_tarif = kt.id)
left join dc_kelas k on (kkt.id_kelas = k.id)
join dc_layanan l on(l.id = kt.id_layanan)
left join dc_layanan ll on(ll.id = l.id_parent) 
left join dc_jenis_pemeriksaan jp on (jp.id = l.id_jenis_pemeriksaan)
left join dc_unit u on (kt.id_unit = u.id)
left join dc_bobot b on (kt.id_bobot = b.id)

where 1  and jp.nama = 'Pelayanan Laboratorium'  and (kt.jenis = 'Rawat Inap'  or kt.jenis is null)  and 
                
*(kkt.id_kelas = 'III' or kkt.id_kelas is null)  

and kt.active = '1' 
and l.nama like ('%%')  limit 0, 20
```

kkt.id_kelas harusnya berisi id bukan literal. 

`sesi 3`  melacak kelas III darimana ia berasal
kelas di set setelah memanggil ini api/admission/pendaftaran_detail

(PATENT)
line 447 k.nama diganti menjadi k.id


`sesi 4`
di printing sesuatu bernama item_laboratorium.  

## Logs
`06.35` start
