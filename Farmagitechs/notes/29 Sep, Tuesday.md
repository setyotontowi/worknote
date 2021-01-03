---
tags: ['2020/[09] September']
title: '29 Sep, Tuesday'
created: '2020-09-29T00:07:55.148Z'
modified: '2020-09-29T07:27:15.872Z'
---

# 29 Sep, Tuesday

`Day 233` The human limit

- [x] Edoc: History edit not match with the design 
- [ ] Edoc: Logout (much)
- [ ] Edoc: Shortcut Document (Main Feature) (Planning)
- [x] Pendaftaran Online: Test Kamera (Hold)

## Task 1
- show and separate created and modified time.
- check API
- check design
- API: doc history list there are modified and created
- in modal dialog, add created and modified time. this also needs redesign layout.

## Task 3
Learn first
- API
- Trello
- Settings

**(Phase 1)**
In Setting, when add shortcut clicked, the modal dialog that contain `addDocument`'s like view shows up. Then after the user choose the documents he desired and click next button, an EditText shows and the user can name the shortcut. Click save to complete process. 
- Tech stack
1. folder like library (ExpandableListView)
2. recycler view selected item (not necessary as in the original design use dropdown instead)
3. [multiple dialog / swipe dialog](https://medium.com/@droidbyme/android-recyclerview-with-single-and-multiple-selection-5d50c0c4c739)  (It also unnecessary)

**(Phase 2)**
For the view, it's like a expandable folder with shortcut name. The given document list, when clicked, show modal to preview the thumbnail. If the shortcut is clicked long enough, then the `add shortcut modal` pops again and the user can edit and delete the list of documents. 

**(Phase 3)**
Then the add document. It forms the recycler view that show the list of shortcuts in horizontal. Then after the documents is created, the activity back to `MainFragment` with updated document list in `PatientFragment`. 

## Task 4
- api provinsi timeout

## Logs
`06.55` init
`09.52` task 1 complete, task 4 hold
