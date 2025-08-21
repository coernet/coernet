---
title: "Markdown Syntax Test Document"
date: 2024-01-15T10:00:00+08:00
draft: false
summary: "Ini adalah dokumen uji yang berisi berbagai sintaks Markdown untuk memverifikasi kelengkapan gaya prosa."
categories: ["Test"]
tags: ["markdown", "prose", "style"]
---

# Heading 1

Ini adalah paragraf dibawah judul level 1.

## Heading 2

Ini adalah paragraf dibawah judul level 2.

### Heading 3

Ini adalah paragraf dibawah judul level 3.

#### Heading 4

Ini adalah paragraf dibawah judul level 4.

##### Heading 5

Ini adalah paragraf dibawah judul level 5.

###### Heading 6

Ini adalah paragraf dibawah judul level 6.

## Paragraf dan Pemformatan Teks

Ini adalah paragraf normal. Ini dapat berisi **teks tebal**, *teks mirring*, ***teks miring tebal***, ~~coretan~~, `inline code`, dan [teks tautan](https://example.com).

Ini adalah paragraf lain untuk menguji jarak antar paragraf.

## Kutipan blok

> Ini adalah kutipan blok sederhana.
> 
> Kutipan blok dapat berisi beberapa paragraf.

> Ini adalah contoh kutipan blok bersarang:

> 
> > Ini adalah konten kutipan bersarang.

> > 
> > Beberapa tingkat bersarang dimungkinkan.


## Daftar

### Daftar Tidak Berurutan

- Item pertama
- Item kedua
  - Item bersarang 1
  - Item bersarang 2
    - Item bersarang yang lebih dalam
- Item ketiga

### Daftar Terurut

1. Item pertama
2. Item kedua
   1. Item pesanan bersarang 1
   2. Item pesanan bersarang 2
      1. Item bersarang yang lebih dalam
3. Item ketiga

### Daftar Tugas (Checkbox)

- [x] Tugas selesai
- [ ] Tugas tidak selesai
- [x] Another completed task
- [ ] Daftar tugas berlapis
  - [x] Subtugas 1 (selesai)
  - [ ] Subtugas 2 (belum selesai)
  - [x] Subtugas 3 (selesai)

### Daftar Definisi

Istilah 1
: Ini adalah definisi untuk istilah 1.

Istilah 2
: Ini adalah definisi untuk istilah 2.
: Istilah dapat memiliki beberapa definisi.

## Kode

### Kode sebaris

Ini adalah paragraf dengan bagian dalam `console.log('Hello World')`.

### Blok Kode

```javascript
function greet(name) {
  console.log(`Hello, ${name}!`);
}

greet('World');
```

```python
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n-1) + fibonacci(n-2)

print(fibonacci(10))
```

```css
.prose {
  max-width: none;
  color: var(--tw-prose-body);
}

.prose h1 {
  font-size: 2.25rem;
  font-weight: 700;
}
```

## Tables

| Menyejajarkan Kiri | Tengah Menyelaraskan | Sejajarkan Kanan |
|:-----------|:------------:|------------:|
| Konten 1  | Konten 2    | Kontetn 3   |
| Konten yang lebih panjang | Sedang    | Pendek       |
| Data A     | Data B       | Data C      |

## Aturan Horisontal


---

## Gambar

![Sample Image](/images/01.avif "Contoh Gambar")

## Links

Ini adalah [Tautan reguler](https://example.com).

Ini adalah [Tautan dengan judul](https://example.com "Link Title").

Ini adalah tautan gaya referensi: [Tautan  referensi][1]

[1]: https://example.com "Reference Link Title"

## Catatan kaki

Ini adalah paragraf dengan catatan kaki1[^1].

Berikut adalah catatan kaki lainnya[^note].

[^1]: Ini adalah isi dari catatan kaki yang pertama.

[^note]: Ini adalah isi dari catatan kaki yang dinamai.

## Teks yang Disorot

Ini adalah paragraf dengan ==teks yang disorot==.

## Superskrip dan Subskrip

H~2~O adalah rumus kimia untuk air.

E = mc^2^ adalah persamaan massa-energi Einstein.

## Tombol Keyboard

Tekan <kbd>Ctrl</kbd> + <kbd>C</kbd> untuk menyalin teks.

## Singkatan

HTML adalah singkatan dari  *HyperText Markup Language*.

*[HTML]: Bahasa Markup HyperText

## Rumus Matematika (jika KaTeX didukung)

Rumus sebaris: $E = mc^2$

Rumus blok:

$$
\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
$$

## Peringatan (jika didukung)

> [!NOTE]
> Ini adlah catatan.

> [!TIP]
> Ini adlah tip.

> [!IMPORTANT]
> Ini adlah informasi penting.

> [!WARNING]
> Ini adalah peringatan.

> [!CAUTION]
> Ini adalah peringatan.

## Detail (jika didukung)

<details>
<summary>Klik untuk memperluas detail</summary>

Ini adalah konten terperinci yang diciutkan.

Anda dapat menyertakan sintaks Markdown apa pun di sini:

- Dafatar Item
- **Teks Tebal**
- `Code`

</details>

## Tes Konten Campuran

Paragraf ini berisi beberapa format: **tebal**, *miring*, `code`, [tautan](https://example.com), ~~dicoret~~, ==sorotan==.

### Daftar Kompleks

1. Item pertama dengan teks **tebal**
   - Item bersarang dengan `code`
   - Item bersarang lainnya dengan [tautan](https://example.com)
2. Item kedua dengan teks *miring*
   1. Item bersarang yang dipesan
   2. Item bersarang lain yang dipesan
3. Item ketiga dengan teks ~~yang dicoret~~

### Tabel Kompleks

| Fitur | Keadaan | Deskripsi         |
|---------|:------:|--------------------|
| **Tebal** | ✅    | Mendukung teks tebal |
| *Miring* | ✅    | Mendukung huruf miring    |
| `Code`   | ✅    | Mendukung kode sebaris |
| [Toutan](https://example.com) | ✅ | Mendukung tautan |
| ~~Coretan~~ | ❌ | Perlu diuji   |

Dokumen pengujian ini mencakup sintaks Markdown yang paling umum dan dapat digunakan untuk memverifikasi kelengkapan dan estetika gaya prosa.

