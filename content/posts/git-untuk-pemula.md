---
title: 'Apa itu Git dan Kenapa Penting bagi Programmer?'
date: 2025-08-22T21:35:21+07:00
draft: false
slug: git untuk pemula
description:
summary:
tags: ["Tutorials", "Git"]
categories: ["Git"]
cover: '/images/placeholder/git/git-petanikode.png'
---


Git adalah salah satu tool yang sering digunakan dalam proyek pengembangan software.

Git bahkan menjadi tool yang wajib dipahami oleh programmer, karena banyak digunakan di mana-mana.

Pada kesempatan ini kita akan belajar Git dari dasar.

Artikel ini hanya akan membahas pengenalan Git saja. Untuk mempelajari Git lebih lanjut, saya sudah menyediakan link di bagian akhir.

## Mengenal Git

Git adalah salah satu sistem pengontrol versi (Version Control System) pada proyek perangkat lunak yang diciptakan oleh Linus Torvalds.

Pengontrol versi bertugas mencatat setiap perubahan pada file proyek yang dikerjakan oleh banyak orang maupun sendiri.

Git dikenal juga dengan distributed revision control (VCS terdistribusi), artinya penyimpanan database Git tidak hanya berada dalam satu tempat saja.

{{< figure
  src="/images/placeholder/git/sistem-git.png"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}

Semua orang yang terlibat dalam pengkodean proyek akan menyimpan database Git, sehingga akan memudahkan dalam mengelola proyek baik online maupun offline.

Dalam Git terdapat merge untuk menyebut aktifitas penggabungan kode.

Sedangkan pada VCS (Version Control System) yang terpusat… database disimpan dalam satu tempat dan setiap perubahan disimpan ke sana.

{{< figure
  src="/images/placeholder/git/vcs-terpusat.png"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}

VCS terpusat memiliki beberapa kekurangan:
- Semua tim terkoneksi ke jaringan untuk mengakses source-code.
- Tersimpan di satu tempat, nanti kalau server bermasalah bagaimana?

Kerana itu, Git Hadir untuk menutup kekurangan yang dimiliki oleh VCS terpusat.


### Apa yang dilakukan oleh GIt?

Git sebenarnya akan memantau semua perubahan yang terjadi pada file proyek. Lalu menyimpannya ke dalam database.

Sebelum menggunakan Git:

{{< figure
  src="/images/placeholder/git/revisi-tanpa-git.png"
  alt="Petani Kode"
  link="#"
  caption="Revisi Tanpa Git"
  class="ma0 w-75"
>}}

Setelah menggunakan Git:

{{< figure
  src="/images/placeholder/git/database-git.png"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}

Apa perbedaannya?

Saat kita ingin menyimpan semua perubahan pada file, biasanya kita membuat file baru dengan “save as”. Lalu, file akan menumpuk dalam direktori proyek seperti pada ilustrasi di atas.

Tapi setelah menggunakan Git…

Hanya akan ada satu file dalam proyek dan perubahannya disimpan dalam database.

Git hanya akan menyimpan delta perubahannya saja, dia tidak akan menyimpan seluruh isi file yang akan memakan banyak memori.

Git memungkinkan kita kembali ke versi revisi yang kita inginkan.

### Kenpa Git Penting Bagi Programes?

{{< figure
  src="/images/placeholder/git/jutsu-kolaborasi.jpg"
  alt="Petani Kode"
  link="#"
  caption="Sistem Git"
  class="ma0 w-75"
>}}

Jadi selain untuk mengontrol versi, git juga digunakan untuk kolaborasi.

Saat ini Git menjadi salah satu tool terpopuler yang digunakan pada pengembangan software open source maupun closed source.

Google, Microsoft, Facebook dan berbagai perusahaan raksasa lainnya menggunakan Git.

Jadi, buat kamu yang punya impian ingin bekerja di sana, maka kamu harus bisa Git.

{{< link id="github" >}}

Selain itu, berikut ini ada beberapa menfaat yang akan kamu rasakan setelah bisa menggunakan Git.

1. Bisa menyimpan seluruh versi source code;
2. Bisa paham cara kolaborasi dalam proyek;
3. Bisa ikut berkontribusi ke proyek open-source;
4. Lebih aman digunakan untuk kolaborasi, karena kita bisa tahu apa yang diubah dan siapa yang mengubahnya.
5. Bisa memahami cara deploy aplikasi modern;
6. Bisa membuat blog dengan SSG.
7. dan sebagainya…

### Apa Selanjutnya?
Jadi, apakah kamu sudah mengenal git?

Bagus, selanjutnya silakan ikuti tutorial git berikut ini.

- [Tutorial Git #01: Cara Install Git dan Konfigurasi Awal yang harus dilakukan](#)
- [Tutorial Git #02: Membuat Repositori Baru dalam Proyek](#)
- [Tutorial Git #03: Membuat Revisi dan Menyimpannya dengan Git Commit](#)
- [Tutorial Git #04: Melihat Catatan Log Revisi Git](#)
- [Tutorial Git #05: Melihat Perbandingan Revisi Git](#)
- [Tutorial Git #06: Membatalkan Revisi Git](#)
- [Tutorial Git #07: Menggunakan Percabangan untuk Mencegah Konflik](#)
- [Tutorial Git #08: Perbedaan Git Checkout, Git Reset, dan Git Revert](#)
- [Tutorial Git #09: Bekerja dengan Remote Repositori](#)
- [Tutorial Git #10: Kolaborasi dengan Tim pada Proyek Open Source](#)
- [Tutorial Git #11: Git Tag](#)

**P.S**: Kalau link di atas masih mati, berarti masih dalam draf. Sering-sering dicek agar tidak ketinggalan. 😄

📖 Referensi:

[https://git-scm.com/](https://git-scm.com/)

[https://en.wikipedia.org/wiki/Git](https://en.wikipedia.org/wiki/Git)