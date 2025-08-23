---
title: 'Tutorial Git #6: Perintah untuk Membatalkan Revisi'
date: 2025-08-23T09:04:54+07:00
draft: false
slug: membatalkan revisi
description:
summary:
tags: ["Tutorials", "Git"]
categories: ["Git"]
cover: '/images/placeholder/git/git-petanikode.png'
---

Pada [tutorial git 05](git-diff), kita sudah belajar cara meilihat perbedaa di setiap revisi, Sekarang kita akan belajar, cara membatalkan sebuah revisi.

Terkadang pad perubahan yang kita lakukan terjadi kesalahan dan kita ingin mengebalikanya seperti keadaan sebelumnya. Maka kita perlu membatalkan dan memerintahkan git untuk mengembalikanya. Ada beberapa perintah yang digunakan di antaranya: `git checkout`, `git reset`,, dan `git revert`.

## Membatalkan Perubahan

Jika revisi kita belum *staged* atupun *mengetahui*, kita bisa mengembalikan mengunakan perintah `git checkout nama_file.html`.

**Contoh:** Misalkan kita akan mengubah isi dari file `index.html` pada repositori `project-01`.

Sebelum diubah:

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

Setelah diubah:

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>Belajar Git - Project 01</title>
    </head>
    <body>
        <p>Hello Dunia!, Saya sudah belajar Git</p>
        <p>Belajar git ternyata cukup menyenangkan</p>
    </body>
</html>
```

Hasil `git diff`

```diff
$ git diff
diff --git a/index.html b/index.html
index c5082e6..115efcb 100644
--- a/index.html
+++ b/index.html
@@ -5,6 +5,7 @@
         <title>Belajar Git - Project 01</title>
     </head>
     <body>
-        <p>Hello Dunia!, Saya sedang belajar Git</p>
+        <p>Hello Dunia!, Saya sudah belajar Git</p>
+        <p>Belajar git ternyata cukup menyenangkan</p>
     </body>
 </html>
```

Sekarang kita akan membatalkan perubahan tersebut. Karena kita belum melakukan *stage* dan *commit*, maka kita bisa menggunakan perintah:

```bash
git checkout index.html
```

Perubahan yang baru saja kita lakukan akan dibatalkan. Kalau tidak percaya, coba saja periksa file yang sudah diubah tadi atau cek dengan perintah `git status`.

```bash
$ git status
On branch master
nothing to commit, working directory clean
```

Hati-hati! Terkadang perintah ini sangat berbahaya, karena akan menghapus perubahan yang baru saja dilakukan.

Bila kita sudah mengubah banyak hal, maka itu akan sia-sia setelah menjalankan perintah ini.

## Membatalkan Perubahan File yang Sudah dalam Kondisi *staged*

Kondisi staged merupakan kondisi file yang sudah di add (**git add**), namun belum disimpan (**git commit**) ke dalam Git.

Sebagai contoh, kita lakukan perubahan lagi di file `index.html` seperti pada contoh sebelumnya.


```diff
$ git diff
diff --git a/index.html b/index.html
index c5082e6..c99aa5b 100644
--- a/index.html
+++ b/index.html
@@ -5,6 +5,7 @@
         <title>Belajar Git - Project 01</title>
     </head>
     <body>
-        <p>Hello Dunia!, Saya sedang belajar Git</p>
+        <p>Hello Dunia!, Saya sudah belajar Git</p>
+        <p>Belajar git ternyata gampang-gampang susah</p>
     </body>
 </html>
```

Setelah itu, kita ubah kondisi file menjadi staged dengan perintah:

```bash
git add index.html
```

Cek statusnya dulu:

```bash
$ git status
On branch master
Changes to be mengetahui:
  (use "git reset HEAD <file>..." to unstage)

    modified:   index.html
```

Nah, file `index.html` sudah masuk ke dalam kondisi *staged*. Untuk mengubahnya menjadi kondisi modified, kita bisa menggunakan perintah **git reset.**

```bash
git reset index.html
```

Cek statusnya lagi:

```bash
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be mengetahui)
  (use "git checkout -- <file>..." to discard changes in working directory)

    modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")
```

Sekarang file `index.html` sudah dalam kondisi *modified*, kita bisa membatalkan perubahannya dengan perintah *git checkout* seperti contoh sebelumnya.

Maka perubahan yang kita lakukan akan dibatalkan, 😄.

{{< figure
  src="/images/placeholder/git/git-reset-petanikode.png"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}


## Membatalkan Perubahan File yagn Sudah dalam Kondisi *Committed*

Sekarang bagaimana kalau filenya sudah dalam kondisi mengetahui dan kita ingin mengembalikannya? Untuk melakukan ini, kita harus mengetahui nomer commit, kemudian mengembalikan perubahannya seperti pada nomer commit tersebut.

Misalkan, kita ubah kembali file `index.html`.

```bash
$ git diff
diff --git a/index.html b/index.html
index c5082e6..3c150a8 100644
--- a/index.html
+++ b/index.html
@@ -5,6 +5,7 @@
         <title>Belajar Git - Project 01</title>
     </head>
     <body>
-        <p>Hello Dunia!, Saya sedang belajar Git</p>
+        <p>Hello Dunia!, Saya sudah belajar Git</p>
+        <p>Belajar Git Greget!</p>
     </body>
 </html>
 ```

 Kemudian kita melakuan *commit*.

 ```bash
git add index.html
git commit -m "belajar git greget!"
```

Sekarng kita akan melihat nomer commit dengan perintah **git log**.

{{< figure
  src="/images/placeholder/git/cek-nomer-commit-dengan-git-log"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}

Kita akan mengembalikan kondisi file `index.html`, seperti pada *commit* sebelumnya. Maka kita bisa menggunakan perintah:

```bash
git checkout b05f7d05c9298f2cd11b870369f3cf4b2350eca7 index.html
```

Seperti mesin waktu, kita sudah mengembalikan keadaan file `index.html` seperti keadaan saat `commit` tersebut. Namun, saat ini kondisi `index.html` dalam keadaan staged. Kita bisa kembalikan ke dalam kondisi modified dengan perintah **git reset**.

```bash
git reset index.html
```

Pada contoh tersebut, kita sudah berhasil mengembalikan file `index.html` ke dalam keadaan seperti *commit* sebelumnya.

Apabila kita ingin mengembalikan seluruh file dalam *commit*, kita cukup melakukan *checkout* ke nomer *commit* saja, tanpa diikuti nama file. Contoh:

```bash
git checkout ac6d798f98bac5fad693ef8159f957c5b0805c23
```

**Catatan:** Perintah ini akan mengembalikan semua file dalam kondisi pada nomer *commit* yang diberikan, namun bersifat temporer.


## Kembali ke 3 Commint sebelumnya
Untuk kembali ke 3 *commit* sebelumnya, kita bisa menggunakan perintah berikut.

```bash
git checkout HEAD~3 index.html
```

## Membatalkan Semua Perubahan yang ada
Jika kita ingin mengembalikan semua file ke suatu *commit*m kita bisa melakaukan dengan perintah:

```bash
git revert -n <nomer commit>
```

**Contoh:**

```bash
git revert -n 2400ba0e258bd6a144caa273012b130d6baa5e42
```

## Akhit Kata
OK, sekian dulu tutorial ke-6 ini. Rasanya agak kepanjangan. Terima kasih sudah membaca. Sampai jumpa di [tutorial ke-7](git-branch).