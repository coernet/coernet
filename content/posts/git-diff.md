---
title: 'Tutorial Git #5: Melihat Perbandingan Revisi dengan Git Diff'
date: 2025-08-23T08:49:06+07:00
draft: false
slug: git diff
description:
summary:
tags: ["Tutorials", "Git"]
categories: ["Git"]
cover: '/images/placeholder/git/git-petanikode.png'
---

Pada tutorial sebelumnya, kita sudah belajar car melihat revisi di repositori. Sekarang kita akan pelajari perintah `git diff`, fungsinya untuk melihat perbedaan perubahan pada di revisi.

## Melihat Perbadingan Perubahan yang Dilakaukan Pada Revisi

Gunakan perintah berikut ini untuk melihat perubahan yang dilakukan pada revisi tertentu.

```bash
git diff cf08ca0837cf26f1c595be36bb3a6b815e311be1
```

`cf08ca0837cf26f1c595be36bb3a6b815e311be1` adalah nomer revisi yang ingin dilihat.

{{< figure
  src="/images/placeholder/git/Git-diff-pada-nomer-revisi.png"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}

Lihatlah hasil di atas, simbol plus `(+)` artinya kode yang ditambahkan. Sedangkan kalau ada kode yang dihapus simbolnya akan menggunakan minus `(-)`.

**Contoh:**

Ditambahkan:
```diff
+ <p> ini kode yangditambahkan</p>
```

Dihapus:
```diff
- <i>ini kode yang dihapus</i>
```

Dimodifikasi/diubah:
```diff
- <span>ini kode sebelum diubah</span>
+ <span>ini kode sesudah diubah</span>
```

Sekarang kita akan mencoba mengubah isi dari `index.html`.

Sebelum diubah:

```html
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

Setelah diubah:

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>Belajar Git - Project 01</title>
    </head>
    <body>
        <p>Hello Dunia!, Saya sedang belajar Git</p>
    </body>
</html>
```

Setelah itu lakukan perintah `git diff` lagi.

{{< figure
  src="/images/placeholder/git/perbedaan-revisi"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}

Apa yang dilakukan `git diff`? Perintah `git diff` akan membandingkan perubahan yang baru saja dilakukan dengan revisi/*commit* terakhir.


### Melihat perubahan Perbandingan pada File

Apabila kita melakukan banyak perubahan, makan akan banyak sekali tampilan output, Karena itu, kita mungkin hanya perlu melihat perubahan untuk file tertentu saja. Untuk melihat perbadingan perubahan pada file tertentu, gunakan perintah berikut.

```bash
git diff index.html
```

Perintah diatas akan melihat perbedaa perubahan pada file `index.html` saja.


## Melihat Perbadingan antara Revisi/Commit

Perintah untuk membandingkan perubahan pada revisi dengan revisi yang lain adalah sebagai berikut.

```bash
git diff <nomer commit> <nomer commit>
```

**Contoh:**
```bash
git diff cf08ca0837cf26f1c595be36bb3a6b815e311be1 06f735af7724558164c87f6b1ce3ca7778eb1c1b
```

## Perbadingan Antara Cabang (Branch)
Kita memang belum masuk ke materi percabangan di Git. Tapi tidak ada salahnya mengetahui cara melihat perbandingan perubahan antar cabang.

```bash
git diff <nama cabang> <nama cabang>
```

## Penutup
Kita sudah pelajari fungsi dari perintah gi`t diff`. Perintah ini untuk melihat perbandingan perubahan apa saja yang telah dilakukan pada repositori. Selanjutnya, kita akan belajar membatalkan revisi.

Selanjutnya: [Tutorial Git 06 - Membatalkan Revisi]()