---
tags: ['2020/[09] September']
title: '4 Sep, Friday'
created: '2020-09-04T01:58:20.910Z'
modified: '2020-09-04T03:53:14.718Z'
---

# 4 Sep, Friday

`Day 216` fainthearted

- SIMRS V2
- [ ] New Features: Pembuatan Fitur Rekap Pendapatan Per Layanan (BZ6lgmj)

## Pembuatan Fitur Rekap Pendapatan Per Layanan
### The Briefing
Here's the short brief:
So: Rekap layanan per kunjungan pasiennya
entah itu dari poli terus transfer ke ranap. jadi intinya melacak layanan tersebut. 

Tracing, from the very beginning
Then compare, **what it should be**.

Find Pasien Rawat Inap, (they include, layanan in top of billing)
so, they summarize all in the end of billing.

and the output feature is become clearer now
as the name "Rekap Pendapatan Per Layanan" (clear)

### The Planning
Similar to query that constructed the Billing, you can collect information about Layanan and track their origin.

**Scribble**
api/keuangan/rekap_billing_data
m_keuangan/get_pendaftaran_detail (keypoint)
id_pendaftaran 4426
jenis_layanan -> enum (poli, igd, ranap, mcu, lab, rad, fisio, forensik, hemo, kemo) -> first pop up
vocab test
http://testyourvocab.com/result?user=14476521


## Logs
`07.49` init
`09.57` the briefing summary complete with understanding.

