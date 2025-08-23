---
title: 'Tutorial Git #4: Melihat Catatan Log Revisi'
date: 2025-08-23T08:34:52+07:00
draft: false
slug: git log
description:
summary:
tags: ["Tutorials", "Git"]
categories: ["Git"]
cover: '/images/placeholder/git/git-petanikode.png'
---

Pada [Tutorial Sebelumnya](git-commit), kita sudah membuat dua revisi oada repositori `project-01`. Sekarang bagaimana cara kita meilhat catatab log dari revisi tersebut?

Git sudah menyediakan perintag `git log` untuk melihat catatan perubahan pada repositori. Contoh Penggunaanya:

```bash
git log
```

Maka kita akan melihat log perubahan apa saja yang sudah kita lakukan dalam repositori.

{{< figure
  src="/images/placeholder/git/Log-revisi-yang-sudah-dibuat.png"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}

Pada gambar diatas, terdapat dua revisi perubahan yang dilakukan .

## Log yang Lebih Pendek

untuk menapilkan log yang lebih pendek, kita bisa menabahan argumen `--online`.

```bash
git log --online
```

Maka akan menghasilkan output:

```bash
06f735a ditambahkan isi
cf08ca0 commit pertama
```

## Log pada Nomer Revisi/*Commit*
Untuk meilihat log pada revisi tertentu, kita bisa memasukan nomer revisi/*commit*.

```bash
git log cf08ca0837cf26f1c595be36bb3a6b815e311be1
```

Maka akan menghasilkan output:

```bash
commit cf08ca0837cf26f1c595be36bb3a6b815e311be1
Author: Ardianta Pargo <ardianta_pargo@yahoo.co.id>
Date:   Mon Feb 13 18:08:56 2017 +0800

    commit pertama
```

## Log pada File Tertentu

Utnuk melihat revisi pada file tertentu, kita dapa memasukan nama filenya.

```bash
git log index.html
```

Maka akan menghasilkan output:

```bash
commit 06f735af7724558164c87f6b1ce3ca7778eb1c1b
Author: Ardianta Pargo <ardianta_pargo@yahoo.co.id>
Date:   Mon Feb 13 18:26:50 2017 +0800

    ditambahkan isi

commit cf08ca0837cf26f1c595be36bb3a6b815e311be1
Author: Ardianta Pargo <ardianta_pargo@yahoo.co.id>
Date:   Mon Feb 13 18:08:56 2017 +0800

    commit pertama
```

Karena file `index.html sudah direvisi sebanyak dua kali.

## Log Revisi yang dilakukan oleh Auhtor Tertentu

Misalkan dalam repositori dikerjakan oleh banyak orang. Maka kita dapa melihat revisi apa saja yang dilakukan oleh orang tertentu dengan perintah berikut.

```bash
git log --auhtor='example'
```

## Penutup

Itulah beberapa cara melihat log revisi pada repositoru. Perintah yang dugunakan adalah `git log`. Selanjutnya kita akan pelajari `git diff` untuk melihat perbandingan pada revisi.

Selanjutnya: [Tutoria Git 05-Melihat Perbandingan revisi](git-diff)