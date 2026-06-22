---
title: Sintaks Dasar & Selector
layout: default
parent: CSS
nav_order: 1
---

# CSS — Sintaks Dasar & Selector
{: .no_toc }

<details open markdown="block">
<summary>Daftar Isi</summary>
{: .text-delta }
1. TOC
{:toc}
</details>

---

## Cara Menyisipkan CSS

```html
<!-- Cara 1: Inline (langsung di elemen — hindari) -->
<p style="color: red; font-size: 16px;">Teks merah</p>

<!-- Cara 2: Internal (di dalam <head>) -->
<style>
  p { color: blue; }
</style>

<!-- Cara 3: External (file terpisah — direkomendasikan) -->
<link rel="stylesheet" href="style.css">
```

---

## Struktur CSS

```css
/* Selector { properti: nilai; } */

p {
  color: red;         /* warna teks */
  font-size: 16px;    /* ukuran font */
  margin: 10px;       /* jarak luar */
}
```

---

## Selector

```css
/* Selector Elemen — semua tag <p> */
p {
  color: blue;
}

/* Selector Class — semua elemen dengan class="judul" */
.judul {
  font-size: 24px;
  font-weight: bold;
}

/* Selector ID — elemen dengan id="header" (unik!) */
#header {
  background-color: #333;
  color: white;
}

/* Selector Kombinasi */
.card p {          /* <p> di dalam .card */
  margin: 0;
}

.btn:hover {       /* .btn saat di-hover */
  background: darkblue;
}

.input:focus {     /* .input saat diklik/fokus */
  border-color: blue;
}
```

---

## Warna

```css
.contoh {
  /* Nama warna */
  color: red;
  color: blue;
  color: transparent;

  /* Hex (paling umum) */
  color: #ff0000;    /* merah */
  color: #333333;    /* abu-abu gelap */
  color: #fff;       /* putih (shorthand) */

  /* RGB */
  color: rgb(255, 0, 0);         /* merah */
  color: rgba(0, 0, 255, 0.5);  /* biru 50% transparan */

  /* HSL (modern) */
  color: hsl(0, 100%, 50%);     /* merah */
}
```

---

## Typography

```css
.teks {
  font-family: 'Roboto', Arial, sans-serif;
  font-size: 16px;       /* atau: 1rem, 1.2em */
  font-weight: bold;     /* atau: 400 (normal), 700 (bold) */
  font-style: italic;
  line-height: 1.6;      /* jarak antar baris */
  text-align: center;    /* left | right | center | justify */
  text-decoration: underline;  /* none | underline | line-through */
  text-transform: uppercase;   /* lowercase | capitalize */
  letter-spacing: 2px;
}
```

---

## Box Model

Setiap elemen HTML adalah sebuah "kotak":

```
┌─────────────────────────────┐
│           margin            │
│   ┌─────────────────────┐   │
│   │       border        │   │
│   │   ┌─────────────┐   │   │
│   │   │   padding   │   │   │
│   │   │  ┌───────┐  │   │   │
│   │   │  │content│  │   │   │
│   │   │  └───────┘  │   │   │
│   │   └─────────────┘   │   │
│   └─────────────────────┘   │
└─────────────────────────────┘
```

```css
.kotak {
  /* Ukuran konten */
  width: 300px;
  height: 200px;

  /* Padding (jarak dalam) */
  padding: 20px;              /* semua sisi */
  padding: 10px 20px;         /* atas-bawah | kiri-kanan */
  padding: 10px 15px 20px 25px; /* atas | kanan | bawah | kiri */

  /* Border */
  border: 2px solid #333;
  border-radius: 8px;         /* sudut melengkung */

  /* Margin (jarak luar) */
  margin: 10px;
  margin: 0 auto;             /* tengahkan elemen */
}
```

---

## Display

```css
/* Block — elemen memenuhi lebar penuh, mulai baris baru */
div { display: block; }

/* Inline — elemen mengikuti aliran teks */
span { display: inline; }

/* Inline-block — inline tapi bisa atur width/height */
.badge { display: inline-block; }

/* None — sembunyikan elemen */
.tersembunyi { display: none; }

/* Flex — layout modern (lihat halaman Flexbox) */
.container { display: flex; }
```
