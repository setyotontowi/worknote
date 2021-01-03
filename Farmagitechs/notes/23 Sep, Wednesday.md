---
tags: ['2020/[09] September']
title: '23 Sep, Wednesday'
created: '2020-09-23T00:35:39.757Z'
modified: '2020-09-24T00:18:53.126Z'
---

# 23 Sep, Wednesday

`Day 229` Properly use your 140 IQ

What are we gonna do RN? Test what we did yesterday on real device. Then, do the stage one migration to MVVM, Login part. 

- [x] Edoc: Phase 1 Migration
- [ ] Edoc: Phase 2 Migration
- [x] Edoc: Testing Room persistence for thumbnail in a real device
- [x] Edoc: Force close at 09.23
- [x] Edoc: Lag and choppy when scrolling AddDocument 

## Task 1
- LoginRepository (complete)
- LoginViewModel (complete)
- LoginFragment Adjustment

## Task 2
This can be tricky. I plan to do it on ListPasien as whole. But, I still not understand enough of the usage ViewModel. 

Oh, Keep in mind you should do the migration on edoc-app-research

## Task 3
the easiest way: reinstall (uninstall and reinstall).
applying the 10 quality compression to keep the app runs without lagging.

## Task 4
Assumption: switching server procedure. from Room Persistence that run in main thread.
So, consider it done. We solve it with migrating simultaneosly. It also didn't show up anymore as well.

## Task 5
https://stackoverflow.com/questions/59002056/ui-lags-and-is-choppy-when-using-glide-to-load-images-in-a-recyclerview

That's.
it reduced when I removed NestedScrollView.

## Logs
`07.03` init
`10.07` task 3 and task 5
`10.46` task 4: consider it done.
