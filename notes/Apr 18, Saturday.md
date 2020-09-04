---
tags: ['2020/[04] April']
title: 'Apr 18, Saturday'
created: '2020-04-18T01:33:50.663Z'
modified: '2020-04-18T22:18:21.479Z'
---

# Apr 18, Saturday

`Additional Day 115`

previous note
pdf renderer berjalan di thread yang berbeda. harus sudah selesai di load baru page width dan height nya diketahui (hipotesis)(hipotesis teruji).

membuat canvas dengan width-height segitu?. overflow of new view. berarti harus mempleajari cara kerja finger paint.
karena pdfview extends di canvas. coba dengan menyisipkan text view (teruji). 

image ke pdf juga sepertinya sudah bisa. tapi itu membuat pdf yang benar-benar baru. apakah bisa menempelkan sesuatu ke pdfnya?

sayangnya, PDF Viewer menggunakan Pdfium jadi formatnya berbeda. 
apa diganti menjadi pdfviewer nya google?
di main activity ada contoh untuk membuat pdf, di kelas FileSource juga ada contoh untuk membuat pdf dokumen dari file.
PdfiumCore.newDocument (ParcelFileDescriptor.open(File file. READ ONLY)) where file is pdf file

PdfDocument telah didapatkan. 
problem selanjutnya, width and page dari canvas dan pdf.
problem selanjutnya, mergin canvas and PdfDocument.
jika membuat sesuatu yang baru, memakai startPage, 


## Logs
`08.34` start working

