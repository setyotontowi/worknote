---
tags: ['2020/[08] August']
title: '24 Aug, Monday'
created: '2020-08-24T01:01:08.218Z'
modified: '2020-08-25T01:04:46.114Z'
---

# 24 Aug, Monday

`Day 207` Warmest Regards

- [x] Edoc: Warm up
- [x] Edoc: Regarding camera
- Edoc: Regarding rotation image, and also crop: Research first (tomorrow)
- [ ] Edoc: Issues: brush color and size. (tomorrow)
- Edoc: Cleaning code

## Task 1
check repo. 
perhaps, you want to clean the code first.
testing, likely there were errors back then.

On Second thought. My codes had low readibility. 
Assumption: error happened when add new document via camera. anyway. check first.

Bug list.
- Label not working. (from camera only)
- Check id's of forms respectively. (from camera only). merged above.
- Assumption, camera's bytearray. (task 2)

What shuold be checked, from PasienFragment -> AddDocumentActivity, check bundles

## Task 2
unexpected code 500: 
check API Document.

- somehow, add camera was successfully sent. It was added. But the pic is empty. (solved, as below issues solved)
- an error occured. AddDocumentActivity has leaked window. this caused because it tried to add dialog after its activity finished -> override onDestroy

## Task 3
Conduct research first.
the candidates:
- OpenCV
- Manually cropping image and rotation
- Search for another libraries

Decision: Create dummy project for this. 

## Task 5 Unmeasurable
However, We should clean the overall source code first. 
- [x] Select Create Document among the ones in adapter or in activity (through callback?)
- I wonder if I could do something about Dialog



## Logs
`07.08` init
`08.04` start task 1
`09.29` task 1 complete
`10.19` task 2 complete
`13.45` task 5 subtask 1 complete
