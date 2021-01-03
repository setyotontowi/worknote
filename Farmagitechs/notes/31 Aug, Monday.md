---
tags: ['2020/[08] August']
title: '31 Aug, Monday'
created: '2020-08-31T01:11:52.561Z'
modified: '2020-08-31T03:16:46.405Z'
---

# 31 Aug, Monday

`Day 212` Wake me up when september ends

- Edoc Trivia
- [ ] Confirmation dialog for Hapus Dokumen
- [ ] Notification Handling
- [x] API error handling
- Edoc Adding Many More
- [ ] Regarding add Dokumen Pasien
- [ ] E/AndroidRuntime: FATAL EXCEPTION: main
    Process: id.co.farmagitechs.edoc, PID: 11987
    java.lang.RuntimeException: Unable to start activity ComponentInfo{id.co.farmagitechs.edoc/id.co.farmagitechs.edoc.activities.MainActivity}: android.view.InflateException: Binary XML file line #24: Binary XML file line #24: Error inflating class fragment
        at android.app.ActivityThread.performLaunchActivity(ActivityThread.java:2974)
        at android.app.ActivityThread.handleLaunchActivity(ActivityThread.java:3059)
        at android.app.ActivityThread.-wrap11(Unknown Source:0)
        at android.app.ActivityThread$H.handleMessage(ActivityThread.java:1724)
        at android.os.Handler.dispatchMessage(Handler.java:106)
        at android.os.Looper.loop(Looper.java:164)
        at android.app.ActivityThread.main(ActivityThread.java:7000)
        at java.lang.reflect.Method.invoke(Native Method)
        at com.android.internal.os.RuntimeInit$MethodAndArgsCaller.run(RuntimeInit.java:441)
        at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:1408)
     Caused by: android.view.InflateException: Binary XML file line #24: Binary XML file line #24: Error inflating class fragment
     Caused by: android.view.InflateException: Binary XML file line #24: Error inflating class fragment
     Caused by: java.lang.IllegalStateException: Fragment androidx.navigation.fragment.NavHostFragment did not create a view.
        at androidx.fragment.app.FragmentManagerImpl.onCreateView(FragmentManagerImpl.java:3234)
        at androidx.fragment.app.FragmentController.onCreateView(FragmentController.java:134)
        at androidx.fragment.app.FragmentActivity.dispatchFragmentsOnCreateView(FragmentActivity.java:357)
        at androidx.fragment.app.FragmentActivity.onCreateView(FragmentActivity.java:336)
        at android.view.LayoutInflater.createViewFromTag(LayoutInflater.java:780)
        at android.view.LayoutInflater.createViewFromTag(LayoutInflater.java:730)
        at android.view.LayoutInflater.rInflate(LayoutInflater.java:863)
        at android.view.LayoutInflater.rInflateChildren(LayoutInflater.java:824)
        at android.view.LayoutInflater.rInflate(LayoutInflater.java:866)
        at android.view.LayoutInflater.rInflateChildren(LayoutInflater.java:824)
        at android.view.LayoutInflater.inflate(LayoutInflater.java:515)
        at android.view.LayoutInflater.inflate(LayoutInflater.java:423)
        at android.view.LayoutInflater.inflate(LayoutInflater.java:374)
        at androidx.appcompat.app.AppCompatDelegateImpl.setContentView(AppCompatDelegateImpl.java:555)
        at androidx.appcompat.app.AppCompatActivity.setContentView(AppCompatActivity.java:161)
        at id.co.farmagitechs.edoc.activities.MainActivity.onCreate(MainActivity.java:52)
        at android.app.Activity.performCreate(Activity.java:7258)
        at android.app.Activity.performCreate(Activity.java:7249)
        at android.app.Instrumentation.callActivityOnCreate(Instrumentation.java:1222)
        at android.app.ActivityThread.performLaunchActivity(ActivityThread.java:2927)
        at android.app.ActivityThread.handleLaunchActivity(ActivityThread.java:3059)
        at android.app.ActivityThread.-wrap11(Unknown Source:0)
        at android.app.ActivityThread$H.handleMessage(ActivityThread.java:1724)
        at android.os.Handler.dispatchMessage(Handler.java:106)
        at android.os.Looper.loop(Looper.java:164)
        at android.app.ActivityThread.main(ActivityThread.java:7000)
        at java.lang.reflect.Method.invoke(Native Method)
        at com.android.internal.os.RuntimeInit$MethodAndArgsCaller.run(RuntimeInit.java:441)
        at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:1408)



## Task 3
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
- [x] AddDocumentActivity -> createDocument
- [ ] ~~AddDocumentActivity -> getPdfDoc~~
- [x] DirektoriPasienActivity -> getListKunjungan
- [x] DirektoriPasienActivity -> getListDokumen
- [x] DirektoriPasienActivity -> getListDokumenPasien
- [ ] ~~DirektoriPasienActivity -> getPdfDoc~~
- [ ] ~~DirektoriPasienActivity -> getPdfDocPasien~~
- [ ] ~~DirektoriPasienActivity -> getThumbnailDoc~~ (ignored)
- [ ] ~~DirektoriPasienActivity -> getThumbnailPasien~~ (ignored)
- [x] DocumentActivity -> saveDoc (3)
- [x] DocumentPreviewActivity -> updateAttribute
- [x] DocumentPreviewActivity -> deleteDocument
- [ ] DocumentPreviewActivity -> historyEdit

## Point 2
### Task 1
when added Dokumen Pasien, it went into History Dokumen. recorded in List Tanggal Kunjungan in Direktori Pasien.


## Logs
`07.11` init
