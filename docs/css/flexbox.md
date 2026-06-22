---
title: Flexbox & Grid
layout: default
parent: CSS
nav_order: 2
---

# CSS — Flexbox & Grid
{: .no_toc }

<details open markdown="block">
<summary>Daftar Isi</summary>
{: .text-delta }
1. TOC
{:toc}
</details>

---

## Flexbox

Flexbox adalah cara modern untuk **mengatur layout dalam satu arah** (baris atau kolom).

### Properti Container (Parent)

```css
.container {
  display: flex;

  /* Arah: row (default) | column | row-reverse | column-reverse */
  flex-direction: row;

  /* Rata horizontal: flex-start | flex-end | center | space-between | space-around */
  justify-content: space-between;

  /* Rata vertikal: stretch | flex-start | flex-end | center */
  align-items: center;

  /* Wrap: nowrap (default) | wrap */
  flex-wrap: wrap;

  /* Gap antar item */
  gap: 16px;
}
```

### Properti Item (Child)

```css
.item {
  /* Seberapa besar item tumbuh */
  flex-grow: 1;

  /* Ukuran dasar */
  flex-basis: 200px;

  /* Shorthand */
  flex: 1;           /* grow: 1, shrink: 1, basis: 0 */
}
```

### Contoh: Navbar dengan Flexbox

```css
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 16px 24px;
  background: #333;
}

nav .logo {
  color: white;
  font-size: 20px;
}

nav ul {
  display: flex;
  gap: 20px;
  list-style: none;
}
```

---

## CSS Grid

Grid adalah cara untuk **mengatur layout dalam dua arah** (baris DAN kolom) — cocok untuk layout halaman.

### Dasar Grid

```css
.grid-container {
  display: grid;

  /* Definisi kolom: 3 kolom sama rata */
  grid-template-columns: 1fr 1fr 1fr;

  /* Atau pakai repeat() */
  grid-template-columns: repeat(3, 1fr);

  /* Kolom berbeda ukuran */
  grid-template-columns: 250px 1fr;   /* sidebar + konten */

  /* Definisi baris */
  grid-template-rows: auto;

  /* Gap */
  gap: 20px;
  column-gap: 20px;
  row-gap: 10px;
}
```

### Penempatan Item

```css
.item-besar {
  /* Rentang kolom */
  grid-column: 1 / 3;    /* dari kolom 1 sampai 3 */
  grid-column: span 2;   /* rentang 2 kolom */

  /* Rentang baris */
  grid-row: 1 / 3;
}
```

### Contoh: Layout Blog

```css
.layout {
  display: grid;
  grid-template-columns: 1fr 300px;  /* konten | sidebar */
  grid-template-rows: auto 1fr auto;  /* header | main | footer */
  grid-template-areas:
    "header  header"
    "main    sidebar"
    "footer  footer";
  gap: 20px;
  min-height: 100vh;
}

.header  { grid-area: header; }
.main    { grid-area: main; }
.sidebar { grid-area: sidebar; }
.footer  { grid-area: footer; }
```

---

## Responsive dengan Media Query

```css
/* Default: desktop */
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

/* Tablet (max 768px) */
@media (max-width: 768px) {
  .grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* HP (max 480px) */
@media (max-width: 480px) {
  .grid {
    grid-template-columns: 1fr;
  }
}
```
