---
title: 'Belajar Git #03: Cara Membuat Repositori Git pada Proyek'
date: 2025-08-23T08:13:06+07:00
draft: false
slug: git commit
description:
summary:
tags: ["Tutorials", "Git"]
categories: ["Git"]
cover: '/images/placeholder/git/git-petanikode.png'
---

Pada [tutorial Git yang kedua](git-install), kita sudah membuat repositori kosong. Belum ada apa-apa di sana.

Sekarang coba tambahkan sebuah file baru.

Sebagai contoh, saya akan menambahkan tiga file HTML kosong.

{{< figure
  src="/images/placeholder/git/project-01_repositori-git-petanikode.png"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}

Setelah ditambahkan, coba ketik perintah `git status` untuk melihat status repositorinya.

{{< figure
  src="/images/placeholder/git/Git-status.png"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}

Berdasarkan keterangan di atas, saat ini kita berada cabang (branch) master dan ada tiga file yang belum ditambahkan ke Git.

## Tiga Kelompok Kondisi File dalam Git

sebelum kita membuat revisi, kita akan berkenalan dulu dengan tiga kondisi file dalam Git.

### 1. Modified
Modified adalah kondisi di mana revisi atau perubahan sudah dilakukan, tetapi belum ditandai dan belum disimpan di *version control*. Contohnya pada gambar di atas, ada tiga file HTML yang dalam kondisi *modified*.

### 2. Staged
Staged adalah kondisi di mana revisi sudah ditandai, tetapi belum disimpan di *version control*. Untuk mengubah kondisi file dari modified ke staged gunakan perintah `git add nama_file`. Contoh:

```bash
git add index.md
```

### 3. Commited
Committed adalah kondisi di mana revisi sudah disimpan di version control. perintah untuk mengubah kondisi file dari staged ke *committed* adalah `git commit`.

## Membuat Revisi Pertama
Baiklah, sekarang kita akan sudah tahu kondisi-kondisi file dalam Git. Selanjutnya, silakan ubah kondisi tiga file HTML tadi menjadi staged dengan perintah `git add`.

```bash
git add index.html
git add about.html
git add contact.html
```

Atau kita melakukan seprti ini:

```bash
git add index.html abaout.html contact.html
```

atau:

```bash
git add *.html
```

Atau seperti ini (*semua file dan direktori*):

```bash
git add.
```

Setelah itu, cobalah ketik perintah `git status` lagi. Kondisi filenya sekarang akan menjadi *staged*.

{{< figure
  src="/images/placeholder/git/kondisi-file-staged-di-Git.png"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}

Setelah itu, ubah kondisi file tersebut ke *committed* agar semua perubahan disimpan oleh Git.

```bash
git commit -m "commit pertama"
```

Setelah itu, coba cek dengan perintah `git status` lagi.

{{< figure
  src="/images/placeholder/git/Commit-pertama-git.png"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}

Selamat, revisi pertama sudah kita buat. Selanjutnya cobalah untuk membuat revisi kedua.

## Mebuat Revisi Kedua
Ceritnaya ada perubahana yang akan kita lakukan pada file `index.html`. Silakahkan modifikasi `index.htm`. Sebagai contoh saya mengisi seperti ini.

```bash
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>Belajar Git - Project 01</title>
    </head>
    <body>
        <p>Hello Semua, Saya sedang belajar Git</p>
    </body>
</html>
```
Setelah itu ketik perintah `git statusus`.

{{< figure
  src="/images/placeholder/git/Git-status-revisi-kedua.png"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}

Terlihat disana, file index.html sudah di modifikasi. kondisinya sekarang berada dalam *modified*. Lakukan *commit* lagi seperti revisi pertama.

```bash
git add index.html
git commit -m "ditambahkan isi"
```

Dengan demikian, revisi kedua sudah disimpan oleh Git. Mungkin anda belom tahu maksud dari argumen `-m`, argumen tersebut untuk menambahkan pesan setiap menyimpan revisi.

{{< figure
  src="/images/placeholder/git/timeline-dua-revisi.png"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}

Sekarang Git sudah mencatat revisi yang sudah kita lakukan, Kita bisa ibratakan revisi-revisi ini sebgai *checkpoint* pada Game, Apabila nanti ada kesalahan , kita bisa kembali ke *checkpoint* ini.

Sekian untuk tutorial ke-3 ini, mudah-mudahan bermanfaa.

Selnajutnya: [Tutorial Git 04-Melihat Log Revisi](git-log)