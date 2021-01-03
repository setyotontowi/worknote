---
tags: ['2020/[08] August']
title: '28 Aug, Friday'
created: '2020-08-28T01:03:56.231Z'
modified: '2020-08-31T02:20:05.296Z'
---

# 28 Aug, Friday

`Day 211` The downfall

- Edoc Adding Many More
- [x] Server Setting, inconsistency (ignored)
- [x] Edit Label change to Spinner
- [x] Change Password
- [ ] Regarding add Dokumen Pasien.
- Edoc Trivia
- [ ] Confirmation dialog for Hapus Dokumen
- [ ] Notification Handling
- [x] API error handling

## Notes
Today, Mas Arvin, Bu Ning and Mas Dedy intensively discussed about the next step of this small company. I listened carefully what did those discuss. Mas Dedy, whom more actively talking, has more knowledge about Software Engineering. That makes him a trully Senior Developer. 

My Current Position, in the middle of Junior and Intermediate Programmer. 

## Point 1
### Task 1
so, if we can see it. it's a refinement.

### Task 3
it's bit odd. however, it's not possible if it was worked and suddenly stopped working as time passed. Check it first.

### Task 4
when added Dokumen Pasien, it went into History Dokumen. recorded in List Tanggal Kunjungan in Direktori Pasien

## Point 2
### Task 3
List API's is in 26 Aug. 
Check API in postman respectively (which doable only).

getDoctor -> Nope
getPatient -> Nope
ketika token/session habis. code 401.

API Handler from Response
- [ ] LoginFragment, handling success
- [ ] GeneralHelper -> checkTokenAPI ignored
- [ ] AppSettingFragment -> getDoctor
- [ ] DirektoriPasienFragment -> getPasien
- [ ] FilterFragment -> getDoctor
- [ ] ListPasienFragment -> getPasien 
- [x] PasienFragment -> documentList
- [ ] ~~PasienFragment -> getPdfDoc~~
- [x] PasienFragment -> getPatientDetail
- [x] ProfilFragment -> changePassword
- [x] AddDocumentActivity -> getDocumentType
- [ ] ~~AddDocumentActivity -> getThumbnail (ignored, could disrupting other process)~~
- [ ] AddDocumentActivity -> createDocument
- [ ] AddDocumentActivity -> getPdfDoc
- [ ] DirektoriPasienActivity -> getListKunjungan
- [ ] DirektoriPasienActivity -> getListDokumen
- [ ] DirektoriPasienActivity -> getListDokumenPasien
- [ ] DirektoriPasienActivity -> getPdfDoc
- [ ] DirektoriPasienActivity -> getPdfDocPasien
- [ ] DirektoriPasienActivity -> getThumbnailDoc (ignored)
- [ ] DirektoriPasienActivity -> getThumbnailPasien (ignored)
- [ ] DocumentActivity -> saveDoc (3)
- [ ] DocumentPreviewActivity -> updateAttribute
- [ ] DocumentPreviewActivity -> deleteDocument
- [ ] DocumentPreviewActivity -> historyEdit

## Logs
`07.05` init
`08.54` task 2 complete
`09.25` task 3 complete
`09.51` task 1 complete
