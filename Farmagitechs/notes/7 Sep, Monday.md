---
tags: ['2020/[09] September']
title: '7 Sep, Monday'
created: '2020-09-07T01:08:28.928Z'
modified: '2020-09-07T06:10:41.428Z'
---

# 7 Sep, Monday

`Day 217` Preparation for resignation

- SIMRS V2
- New Features: Pembuatan Fitur Rekap Pendapatan Per Layanan (BZ6lgmj)
- [x] Tracing The Main Query 
- [ ] Tracing The Poli/Ranap
- [ ] Edoc: Filter Poli, Ranap, IGD

## Pembuatan Fitur Rekap Pendapatan Per Layanan
Where was it?

### Wait, Tracing the query?
where item = dc_detail_tarif_tindakan.
or switch case?

assumption
all tables which intended to dc_detail_tarif_T

**The Track: Case Study: Radiologi and Lab**
dc_layanan_pendaftaran -> dc_radiologi -> dc_detail_radiologi -> dc_detail_tarif_radiologi

**The Track: Case Study: Poli dan Ranap(?)**
dc_layanan_pendaftaran -> dc_tarif_tindakan -> dc_detail_tarif_tindakan

**The Track: Case Study: Operasi**
dc_layanan_pendaftaran -> dc_jadwal_kamar_operasi -> dc_tarif_operasi -> dc_detail_tarif_operasi

**The Track: Case Study: Kemoterapi and Hemodialisa**
dc_layanan_pendaftaran -> dc_hemodialisa -> dc_tarif_hemodialisa -> dc_detail_tarif_hemodialisa
empty data

### Yes, I mean it is imperceptible. Tracing Poli/Ranap
from jenis. yes, both have tindakan. 

## Edoc
Filter poli, ranap, igd
- [x] Check in apps
- [x] Check API
- [ ] Search for patients

### Task 1
Creating Getter. 

## Logs
`07.09` init
`10.11` tracing main query complete


