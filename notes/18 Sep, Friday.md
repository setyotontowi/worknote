---
tags: ['2020/[09] September']
title: '18 Sep, Friday'
created: '2020-09-18T00:07:21.612Z'
modified: '2020-09-18T07:03:41.590Z'
---

# 18 Sep, Friday

`Day 226` Regardless

## Early Notes
The server has been rerouted to local server. 
Here's the things we can do:
1. Preloading Thumbnails

How?
1. Add Document Activity (Phase 4)
2. Models, convert it to Entities (Phase 1)
3. Room, Server Dao, Sqlite only for Document Type. (Phase 2)
4. ServerSetting sqlite migration (Phase 3)

Question
1. How to instance App Database in multiple process 
   [Link](https://github.com/fulvmei/FuPlayerForDJ/blob/a54b7d4f431b32c010ce7416c1125baea647480f/library/src/main/java/com/chengfu/android/fuplayer/achieve/dj/audio/db/AudioDatabase.java)

   Implementation
   create a class, or app database getInstance 
   then check if this method is working by testing in ServerSettings.

2. How to implement Document Type thumbnail placeholder
   First step, 

## Logs
`06.56` init
`13.16` 1 convert model to entities (complete)
`13.16` room, server dao (complete)
`13.51` Phase 3 complete
