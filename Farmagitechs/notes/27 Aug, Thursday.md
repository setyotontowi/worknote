---
tags: ['2020/[08] August']
title: '27 Aug, Thursday'
created: '2020-08-27T01:35:05.184Z'
modified: '2020-08-27T07:47:18.307Z'
---

# 27 Aug, Thursday

`Day 210` Internet Down

- Edoc trivia
- [x] 1. Bug, Riwayat Dokumen from Edit
- [x] 2. Check, Riwayat Dokumen from AddDocument
- [ ] 3. Confirmation Dialog for Hapus (nanti)
- [ ] 4. filling more information in Doc's Description -> filename, user (nanti)
- [ ] 5. Do something with brush (nanti)
- [x] 6. Progress Dialog Dismiss on Error Handler Also 4ZIuL2D2
- [x] 7. Error from Camera, its related to MainActivity:52
- Adding Many More fKz62apW
- [x] 8. Edit Undo for the first time. (unable to do anything. restricted method)
- [x] 9. Rincian setelah edit dokumen masih belum sesuai

## Point 1
for edoc, I've been thinking yesterday if we could upload to play store but restricted only to registered email.

### Task 1
try riwayat from add document. 
send back the document

### Task 2
this also, could become a problem.
toasting -> nah, when adding new document, it directs right to Edit.

### Task 7
first clue: after add document.
I tried, to dismiss dialog in TipeDokumenAdapter after adding new document and no signs of bug occurred. 

## Point 2
This is the bugs we found after Maya tested it.

### Task 9
this happens because we only add Dokumen class after PasienFragment. When it comes from AddDocument, it has nothing.
construct own document? or get from API?


## Logs
`07.03` init
`08.36` start
`09.33` task 1 & task 2 complete.
`09.50` task 6 complete
`13.29` task 7 complete
`14.47` task 9 complete
