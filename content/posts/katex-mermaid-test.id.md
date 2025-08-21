---
title: "Tes KaTeX dan Putri Duyung"
date: 2024-01-16T23:30:00+08:00
draft: false
description: "Menguji fitur KaTeX dan Mermaid"
katex: true
mermaid: true
---

# Tes KaTeX dan Putri Duyung

Artikel ini digunakan untuk menguji fitur KaTeX dan Mermaid.

## Konfigurasi

### Konfigurasi Frontmatter
```yaml
---
katex: true
mermaid: true
---
```

### Konfigurasi Global
```yaml
# hugo.yaml
katex:
  enabled: true
  delimiters: 
    - left: "$$"
      right: "$$"
      display: true
    - left: "$"
      right: "$"
      display: false

mermaid:
  enabled: true
```

## Tes KaTeX

### Rumus sebaris

Ini adalah rumus sebaris: $E = mc^2$, kesetaraan massa-energi Einstein.

Contoh Kapan $a \neq 0$, solusi untuk persamaan kuadrat $ax^2 + bx + c = 0$ are $x = \frac{-b \pm \sqrt{b^2-4ac}}{2a}$.

### Rumus Blok

#### Rumus Kuadrat
$$x = \frac{-b \pm \sqrt{b^2-4ac}}{2a}$$

#### Rumus Euler
$$e^{i\pi} + 1 = 0$$

#### Rumus Integral

$$\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}$$

#### Representasi Matriks
$$\begin{pmatrix} a & b \\\\ c & d \end{pmatrix} \begin{pmatrix} x \\\\ y \end{pmatrix} = \begin{pmatrix} ax + by \\\\ cx + dy \end{pmatrix}$$

#### Rumus Penjumlahan
$$\sum_{n=1}^{\infty} \frac{1}{n^2} = \frac{\pi^2}{6}$$

#### Tes Simbol Matematika Umum
Menggunakan makro yang telah ditentukan sebelumnya: $\RR$, $\NN$, $\ZZ$, $\QQ$, $\CC$
