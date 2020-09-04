---
tags: ['2020/[08] August']
title: '5 Aug, Wednesday'
created: '2020-08-05T01:33:51.220Z'
modified: '2020-08-05T04:15:51.823Z'
---

# 5 Aug, Wednesday

`Day 196` Silo

- [x] Edoc: SharedPrefs Issue

## Task 1
masalahnya adalah kita tidak bisa mengkonfigurasi warna dan size secara bersamaan. terdapat tumpang tindih (asumsinya) antara sharedpref yang satu dengan yang lainnya. 

it turns out that multiple method calling can't be executed at same time. It should begin with two different listener for each method execution.

it literally can't executed linearly
temporary solution: leave it like that.



## Logs
`07.35` init
