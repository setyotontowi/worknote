---
tags: ['2020/[08] August']
title: '26 Aug, Wednesday'
created: '2020-08-26T01:08:57.440Z'
modified: '2020-08-28T06:29:25.186Z'
---

# 26 Aug, Wednesday

`Day 209` A twisting whirlwind, as multitasking goes up productivity down

- Edoc: Checking API along with Cleansing Code
- [x] Error Handler, to Toast
- [x] Model Packaging
- [ ] Progress Dialog Dismiss on Error Handler Also 4ZIuL2D2
- [x] Confirm Exit Button 61kqgokj (ignored)
- Regarding NavHost
- Edoc: Trivia
- [ ] Brush and Palletes
- [ ] Check If Online
- [ ] Check If Session is over. both these, perhaps, are using same method
- [x] Riwayat Dokumen from Edit. Caused by document id bundle from DocumentActivity is null.


## Point 1
as I recall, something have to do with API.
- Error handler, to Toast.
- Model Packaging

### Task 1
On Classes
- [x] LoginFragment, handling success
- [x] GeneralHelper -> checkTokenAPI ignored
- [x] AppSettingFragment -> getDoctor
- [x] DirektoriPasienFragment -> getPasien
- [x] FilterFragment -> getDoctor
- [x] ListPasienFragment -> getPasien 
- [x] PasienFragment -> documentList
- [x] PasienFragment -> getPdfDoc
- [x] PasienFragment -> getPatientDetail
- [x] ProfilFragment -> changePassword (2)
- [x] AddDocumentActivity -> getDocumentType
- [x] AddDocumentActivity -> getThumbnail (ignored, could disrupting other process)
- [x] AddDocumentActivity -> createDocument (1)
- [x] AddDocumentActivity -> getPdfDoc
- [x] DirektoriPasienActivity -> getListKunjungan
- [x] DirektoriPasienActivity -> getListDokumen
- [x] DirektoriPasienActivity -> getListDokumenPasien
- [x] DirektoriPasienActivity -> getPdfDoc
- [x] DirektoriPasienActivity -> getPdfDocPasien
- [x] DirektoriPasienActivity -> getThumbnailDoc (ignored)
- [x] DirektoriPasienActivity -> getThumbnailPasien (ignored)
- [x] DocumentActivity -> saveDoc (3)
- [x] DocumentPreviewActivity -> updateAttribute
- [x] DocumentPreviewActivity -> deleteDocument
- [x] DocumentPreviewActivity -> historyEdit

See Documentation for Error Handling? nope, there wasn't. therefore, display toast as it is in ErrorListener.

## Point 2
It seems pointless using NavHost Fragment, I am considering to removing it or taking other action. However, there are many error logs related to MainActivity:52 which is setContentView.
 

## Logs
`07.08` init
`08.09` login to ubuntu
`08.41` task 2 complete
`09.54` task 1 complete

## PTA
- [x] Warming up
- [x] Designing app style, without toolbar, white based
- [x] > Notification color
- [x] Create splash screen
- [x] > Implementing First Page
- [ ] FullScreen App Intro
