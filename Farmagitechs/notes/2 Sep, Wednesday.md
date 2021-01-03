---
tags: ['2020/[09] September']
title: '2 Sep, Wednesday'
created: '2020-09-02T00:44:37.152Z'
modified: '2020-09-02T07:28:40.806Z'
---

# 2 Sep, Wednesday

`Day 214` An ordinary day


## Notes
I become unable to concentrate. Perhaps, due to i'm in the verge of any project as usual. For Edoc, I want to make a radical change that reconstructs the entire codebase. Meanwhile, at the same time, there are two tasks in SIMRS assigned to me plus an Evoluzee preparation for PBG.

alright, now which path will I take?

Requires bravery to switch project. If it should, then I want to switch to Evoluzee, make changes, and publish it in Playstore. Nah, I guess it already done and published in Playstore

Resolving issues in Edoc
- Cleaning the code, I mean from beginning.
Resolving issues in Evoluzee, Pendaftaran Online
- [x] Check API
- [x] Change Logo
- [x] KD Institusi
- [x] Add Crashlytics PKUPBG and Banjar
- [x] Debug Camera on main package
- check API on RMSB
- [x] Publish to Play store

## Task 1: What is it?
Ah, I want experimenting with PR. (clear)

## Debug Camera
E/AndroidRuntime: FATAL EXCEPTION: main
    Process: id.co.farmagitechs.evoluzeepkupbg, PID: 11548
    java.lang.NullPointerException: Attempt to invoke virtual method 'android.content.res.XmlResourceParser android.content.pm.ProviderInfo.loadXmlMetaData(android.content.pm.PackageManager, java.lang.String)' on a null object reference
        at androidx.core.content.FileProvider.parsePathStrategy(FileProvider.java:605)
        at androidx.core.content.FileProvider.getPathStrategy(FileProvider.java:579)
        at androidx.core.content.FileProvider.getUriForFile(FileProvider.java:417)
        at id.co.farmagitechs.evoluzeepkupbg.PasienBaru4.takePhoto(PasienBaru4.java:191)
        at id.co.farmagitechs.evoluzeepkupbg.PasienBaru4$1.onClick(PasienBaru4.java:124)
        at android.view.View.performClick(View.java:6935)
        at android.widget.TextView.performClick(TextView.java:12752)
        at android.view.View$PerformClick.run(View.java:26211)
        at android.os.Handler.handleCallback(Handler.java:790)
        at android.os.Handler.dispatchMessage(Handler.java:99)
        at android.os.Looper.loop(Looper.java:164)
        at android.app.ActivityThread.main(ActivityThread.java:7000)
        at java.lang.reflect.Method.invoke(Native Method)
        at com.android.internal.os.RuntimeInit$MethodAndArgsCaller.run(RuntimeInit.java:441)
        at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:1408)
E/SpellCheckerSession: ignoring processOrEnqueueTask due to unexpected mState=TASK_CLOSE scp.mWhat=TASK_CLOSE

Try test in smartphone instead of tab, using pkupbg. (crash)

(package name in PasienBaru4)

## check API on RMSB
`13.28` ip public mati. 

## Logs
`07.06` init
`09.04` PR experimenting
`13.39` debug camera complete


