---
tags: ['2020/[09] September']
title: '14 Sep, Monday'
created: '2020-09-14T01:56:52.816Z'
modified: '2020-09-14T05:53:29.879Z'
---

# 14 Sep, Monday

`Day 222` Migrating

- [ ] Edoc: Cleansing
- [x] So that, we need Project MVVM
- [ ] Edoc: Debugging

##  Task 1 Cleansing
Architecture
- Activities
  1. AddDocumentActivity
  2. DirektoriPasienActivity
  3. DocumentActivity
  4. DocumentPreviewActivity
  5. LoginActivity
  6. MainActivity
  7. SplashActivity
- Fragments
  1. AppSettingFragment
  2. BrushSettingFragment
  3. DirektoriPasienFragment
  4. DisplaySettingFragment
  5. FilterFragment
  6. ListPasienFragment
  7. LoginFragment
  8. MainFragment
  9. PasienFragment
  10. PlaceholderPasienFragment
  11. ProfilFragment
  12. ServerSettingFragment
  13. SettingFragment

API Handler from Response
- LoginFragment, handling success
- GeneralHelper -> checkTokenAPI ignored
- AppSettingFragment -> getDoctor
- DirektoriPasienFragment -> getPasien
- FilterFragment -> getDoctor
- ListPasienFragment -> getPasien 
- PasienFragment -> documentList
- PasienFragment -> getPdfDoc
- PasienFragment -> getPatientDetail
- ProfilFragment -> changePassword
- AddDocumentActivity -> getDocumentType
- AddDocumentActivity -> getThumbnail (ignored, could disrupting other process)
- AddDocumentActivity -> createDocument
- AddDocumentActivity -> getPdfDoc
- DirektoriPasienActivity -> getListKunjungan
- DirektoriPasienActivity -> getListDokumen
- DirektoriPasienActivity -> getListDokumenPasien
- DirektoriPasienActivity -> getPdfDoc
- DirektoriPasienActivity -> getPdfDocPasien
- DirektoriPasienActivity -> getThumbnailDoc
- DirektoriPasienActivity -> getThumbnailPasien
- DocumentActivity -> saveDoc
- DocumentPreviewActivity -> updateAttribute
- DocumentPreviewActivity -> deleteDocument
- DocumentPreviewActivity -> historyEdit

#### Notes
We still doing the migration. But after the noon, at second batch of work, I choose to go back to fixing bugs and adding features. The trello work. 

## Task 2. Add Document Load multiple thumbnail at once


## Logs
`06.57` init
`12.52` migration option
