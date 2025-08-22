---
title: 'Tutorial Git #1: Cara Install Git dan Konfigurasi Awal yang Harus Dilakukan'
date: 2025-08-22T22:42:58+07:00
draft: false
slug: install git
description:
summary:
tags: ["Tutorials", "Git"]
categories: ["Git"]
cover: '/images/placeholder/git/git-petanikode.png'
---

Kita sudah mengenal Git pada [tulisan sebelumnya](git-untuk-pemula). Selanjutnya Kita akan melakukan instalasi dan persiapan untuk mulai belajar Git.

Tulisan ini terbagi menjadi tiga bagian:

- Cara Instalasi Git di Linux.
- Cara Instalasi Git di Windows.
- Konfigurasi Awal yang Harus dilakukan Setelah Menginstal Git.

Mari kita mulai…

## 1. Cara Install Git di Linux

Instalasi Git pada Distro keluarga Debian dapat menggunakan perintah `apt`.

```bash
sudo apt install git
```

atau

```bash
sudo apt-get install git
```

Pada Fedora:

```bash
yum install git
```

Setalah itu, coba periksa versi yang terinstall dengan perintah:

```bash
git --version
```

Pada komputer saya, versi yang terinstall dengan perintah:

{{< figure
  src="/images/placeholder/git/versi-git-petanikode.png"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}

## 2. Cara Install Git di Windows

Instalasi Git di Windows memang tidak seperti di Linux yang ketik perintah langsung terinstal.

Kita harus men-download dulu, kemudian melakukan ritual *next>next>finish*.

Tapi dalam ritual tersebut, ada pilihan yang harus diperhatikan agar perintah `git` dapat dikenali di CMD.

#### Download Git
Silakan buka website resminya Git [git-scm.com](https://git-scm.com/). Kemudian unduh Git sesuai dengan arsitektur komputer kita. Kalau menggunakan 64bit, unduh yang 64bit. Begitu juga kalau menggunakan 32bit.

#### Langkah-langkah Install Git di Windows
Baiklah, mari kita mulai ritual instalnya. Silakan klik 2x file instaler Git yang sudah diunduh.

{{< figure
  src="/images/placeholder/git/1.Buka-file-instaler-Git.JPG"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git Diwndows"
  class="ma0 w-75"
>}}

Maka akan muncul informasi lisensi Git, klik Next > untuk melanjutkan.

{{< figure
  src="/images/placeholder/git/2.Informasi-tentang-git.JPG"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git Diwndows"
  class="ma0 w-75"
>}}

Selanjutnya menentukan lokasi instalasi. Biarkan saja apa adanya, kemudian klik Next >.

{{< figure
  src="/images/placeholder/git/3.Lokasi-instal.JPG"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git Diwndows"
  class="ma0 w-75"
>}}

Selanjutnya pemilihan komponen, biarkan saja seperti ini kemudian klik Next >.

{{< figure
  src="/images/placeholder/git/4.Pemilihan-komponen.JPG"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git Diwndows"
  class="ma0 w-75"
>}}

Selanjutnya pemilihan direktori start menu, klik Next >.

{{< figure
  src="/images/placeholder/git/5.pembuatan-start-menu.JPG"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git Diwndows"
  class="ma0 w-75"
>}}

Selanjutnya pengaturan *PATH Environment*. Pilih yang tengah agar perintah `git` dapat di kenali di *Command Prompt* (CMD). Setelah itu klik Next >.

{{< figure
  src="/images/placeholder/git/6.Path-environment.JPG"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git Diwndows"
  class="ma0 w-75"
>}}

Selanjutnya konversi *line ending*. Biarkan saja seperti ini, kemudian klik Next >.

{{< figure
  src="/images/placeholder/git/7.konversi-line-ending.JPG"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git Diwndows"
  class="ma0 w-75"
>}}

Selanjutnya pemilihan emulator terminal. Pilih saja yang bawah, kemudian klik Next >.

{{< figure
  src="/images/placeholder/git/8.Pemilihan-emulator-terminal.JPG"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git Diwndows"
  class="ma0 w-75"
>}}

Selanjutnya pemilihan opsi ekstra. Klik saja Next >.

{{< figure
  src="/images/placeholder/git/9.Konfigurasi-Opsi-Ekstra.JPG"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git Diwndows"
  class="ma0 w-75"
>}}

Selanjutnya pemilihan opsi eksperimental, langsung saja klik Install untuk memulai instalasi.

{{< figure
  src="/images/placeholder/git/10.Opsi-ekperimental.JPG"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git Diwndows"
  class="ma0 w-75"
>}}

Tunggu beberapa saat, instalasi sedang dilakukan.

{{< figure
  src="/images/placeholder/git/11.Installing.JPG"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git Diwndows"
  class="ma0 w-75"
>}}

Setelah selesai, kita bisa langsung klik Finish.

{{< figure
  src="/images/placeholder/git/12.Finish.JPG"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git Diwndows"
  class="ma0 w-75"
>}}

Selamat, Git sudah terinstal di Windows. Untuk mencobanya, silakan buka CMD atau PowerShell, kemudian ketik perintah *git --version*.

{{< figure
  src="/images/placeholder/git/versi-git-petanikode.png"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}

### Cara Install Git di MacOS
Buat kamu yang menggunakan MacOS, git bisa diinstal dengan brew.

Buka terminal lalu, ketik perintah berikut untuk menginstal Git:

```zsh
brew install git
```

Tunggulah beberapa saat sampai proses instalasinya selesai. Setelah itu, coba ketik perintah berikut untuk mengecek versi git yang terinstal:

```zsh
git --version
```

Maka hasilnya:


{{< figure
  src="/images/placeholder/git/versi-git-macos.png"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}

Ini artinya, git versi `2.42.0` sudah terinstal dengan benar di MacOS. Selanjutnya, kita bisa lakukan konfigurasi awal.

### 3. Konfigurasi Awal yang Harus Dilakukan
Ada beberapa konfigurasi yang harus dilakukan sebelum mulai menggunakan Git, seperti menentukan *name* dan *email*.

Silakan lakukan konfigurasi dengan perintah berikut ini.


```bash
git config --global user.name "example"
git config --global user.email contoh@exaample.com
```

Kemudian periksa konfigurasinya dengan perintah:

``` bash
git config --list
```

Apabila berhasil tampil seperti gambar berikut ini, berarti konfigurasi berhasil.

{{< figure
  src="/images/placeholder/git/git-config-all.png"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}

Konfigurasi **core.editor** bersifat opsional. Sedangkan name dan email wajib.

Jika kamu memiliki akun Github, Gitlab, Bitbucket atau yang lainnya…

maka username dan *email* harus mengikuti akun tersebut agar mudah diintegrasikan.

Selain konfigurasi awal ini, kamu juga bisa konfigurasi SSH key untuk Github, Gitlab, dan Bitbucket.

Silakan baca caranya di sini:

- [Cara Setup SSH Key untuk Github](#)
- [Cara Setup SSH Key untuk Gitlab](#)
- [Cara Setup SSH Key untuk Bitbucket](#)

### Konfigurasi Default Branch saat ini
Secara default, repository Git akan menggunakan nama branch `master` ketika kita baru pertama membuat repository.

Nama ini sebenarnya mulai ditinggalkan dan disarankan pakai nama `main`. Soalnya di Github.. default branch atau branch utama yang digunakan adalah `main`.

Saat kita mau upload repo ke Github, nantinya kita akan diminta untuk mengubah `master` menjadi `main`.

Biar tidak repot, kita setup aja dari awal.

Lalu gimana caranya supaya Git otomatis menggunakan `main` secara default?

Gampang, kita cukup tambahkan konfigurasi ini.

Silakan ketik di Terminal atau CMD:

```bash
git config --global init.defaultBranch main
```

Dengan demikian, Git akan otomatis menggunakan nama `main` sebagai branch utama.

## Apa Selanjutnya?
Bagus, kita sudah mempersiapkan semuanya. Selanjutnya kita bisa langsung belajar [membuat repositori git](#).