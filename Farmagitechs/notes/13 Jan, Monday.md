---
tags: ['2020/[01] January']
title: '13 Jan, Monday'
created: '2020-01-13T01:41:20.946Z'
modified: '2020-03-19T07:01:59.293Z'
---

# 13 Jan, Monday

`Day 51`

- [ ] 1. Learning SIMRS Khanza
- [ ] 2. Learning Scala
- [ ] 3. SIMRS Dinda : Pembuatan Tombol Edit [link](https://trello.com/c/WhvHmB3R/114-pembuatan-tombol-edit-di-menu-master-data-item-laboratorium)
- [ ] 4. SIMRS Dinda : Error cetak laborat narkoba [link](https://trello.com/c/E66HZc5M/116-eror-saat-cetak-hasil-laborat)

## Task 4
start : `08.52`
Ternyata untuk munculin itu hasil lab harus diisi terlebih dahulu.
end : `09.13`

update : masih ada error
start update `11.08`
masalah, tanggal lahir ada yang belum ke update. di printing/hasil_laboratorium
- kemungkinan pasiennya memang tidak memiliki tanggal lahir. dan sewaktu mengisi form, ada tanggal lahir yang tidak sengaja terkosongkan. kemungkinan, seperti itu.
- tanggal lahir ada dari pasien dengan id_lab = 82010 ada.

di testing / live. nama pasien waryono bin haryono

- yang jelas, ada narkobanya. 
- sudah selesai, cuma belum di update
end : `13.03`

## Task 3 
start `09.14`
tombol edit akan memunculkan modal baru untuk mengedit nilai normalnya.
tombol edit akan mengedit salah satu tabel dengan id tertentu. sayangnya ini array. simpannya ketika tombol simpan di bawah tabel_rule di aktifkan. dengan begitu, tidak ada masalah disitu.
- pembuatan kata-kata di generate semuanya ulang, meskipun hanya satu yang diinputkan.
- kita bisa mengirimkan id_nilai_normal untuk update, di else yang ada di paling bawah. namun kita harus tetap mengirimkan id_item_laboratorium, hanya dalam bentuk satuan. if ini terletak paling awal untuk jaga-jaga

done. sekarang tinggal post action
- refresh dan hide modal

end `11.06`


## Log
`07.25` datang
`08.42` learning android 5 Card UI
`08.52` start task 4
`09.13` task 4 end
`11.06` task 3 end
`11.16` break
`11.37` start
`13.03` task 4 update end
`15.55` pulang
