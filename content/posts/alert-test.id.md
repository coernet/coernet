---
title: "Tes Peringatan Gaya GitHub"
date: 2025-06-01T10:00:00+08:00
slug: uji-peringatan
draft: false
description: "Pengujian Peringatan Gaya GitHub"
tags: ["test", "alert", "markdown"]
categories: ["Github"]
---

# Pengujian Peringatan Gaya GitHub

Artikel ini digunakan untuk menguji fitur Peringatan gaya GitHub baru dan fungsionalitas lipat.

## Sintaks Peringatan

### Peringatan Catatan

> [!NOTE]
> Ini adalah kotak peringatan catatan. Digunakan untuk menampilkan informasi berguna yang harus diperhatikan pengguna, bahkan saat menjelajahi konten dengan cepat.

### Peringatan Tip

> [!TIP]
> Ini adalah kotak peringatan tip. Memberikan saran yang membantu menyelesaikan tugas dengan lebih baik atau lebih mudah.

### Peringatan Penting

> [!IMPORTANT]
> Ini adalah kotak peringatan yang penting. Menampilkan informasi penting yang perlu diketahui pengguna untuk mencapai tujuan mereka.

### Peringatan

> [!WARNING]
> Ini adalah kotak peringatan. Informasi mendesak yang membutuhkan perhatian segera pengguna untuk menghindari masalah.

### Peringatan Perhatian

> [!CAUTION]
> Ini adalah kotak peringatan perhatian. Menyarankan pengguna untuk menyadari risiko atau konsekuensi negatif dari perilaku tertentu.

## Sintaks yang Diperluas - Judul Kustom

### Catatan dengan Judul Kustom

> [!NOTE] Judul Kustom
> Ini adalah kotak peringatan catatan dengan judul khusus.

### Warning with Custom Title

> [!WARNING] Bahaya Radiasi
> Jangan mendekati atau menangani tanpa alat pelindung.

## Fitur Lipat

### Peringatan Lipat yang Diperluas secara Default

> [!TIP]+ Klik untuk menciutkan
> Ini adalah kotak peringatan lipat yang diperluas secara default. Klik judul untuk menciutkan konten.
> 
> Mendukung konten multi-baris:
> - Daftar item 1
> - Daftar item 2
> - Daftar item 3

### Peringatan Terlipat Secara Default

> [!IMPORTANT]- Informasi Penting (Diciutkan secara default)
> Ini adalah kotak informasi penting yang diciutkan secara default. Klik judul untuk memperluas dan melihat konten.
> 
> Dapat mencakup:
> 1. Daftar yang dipesan
> 2. **Teks tebal**
> 3. *Teks miring*
> 4. `Code snippet`

### Peringatan Lipat dengan Konten Kompleks

> [!CAUTION]+ Contoh Konten Kompleks
> Kotak lipat ini berisi konten Markdown yang kompleks:
> 
> #### Subjudul
> 
> Ini adalh paragraf yang berisi [tautan](https://example.com) pemformatan lainya.
> 
> ```javascript
> // Code block example
> function hello() {
>   console.log("Hello, World!");
> }
> ```
> 
> | Table | Example |
> |-------|-------|
> | Baris | Data1 |
> | Baris | Data2 |

## Kutipan Blok Reguler

Ini adalah kutipan blok biasa, bukan Peringatan:

> Ini adalah kutipan blok standar. Ini tidak akan dirender sebagai Peringatan tetapi akan menggunakan gaya blockquote standar.
Mendukung konten multi-baris dan teks yang diformat.
> 
> Mendukung konten multi-baris dan teks yang diformat. **teks yang diformat**.

## Dukungan Multibahasa

Pemberitahuan mendukung beberapa bahasa, dan judul akan ditampilkan secara otomatis dalam bahasa saat ini:

> [!NOTE]
> Dalam lingkungan Cina, judul ini akan ditampilkan sebagai "注意" (Catatan).

> [!TIP]
> Di lingkungan Cina, judul ini akan ditampilkan sebagai "提示" (Tip).

## Pengujian Konten Berlapis

> [!WARNING]+ Pengujian Konten Berlapis
> Pemberitahuan ini berisi konten berlapis:
> 
> > Ini adalah kutipan blok bersarang
> 
> - Item daftar
>   - Item daftar berlapis
>   - Item bersarang lainnya
> 
> 1. Daftar yang dipesan
>    1. Daftar berurutan berlapis
>    2. Item bersarang lainya