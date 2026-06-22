---
title: DOM & Event
layout: default
parent: JavaScript
nav_order: 2
---

# JavaScript — DOM & Event
{: .no_toc }

<details open markdown="block">
<summary>Daftar Isi</summary>
{: .text-delta }
1. TOC
{:toc}
</details>

---

## Apa itu DOM?

**DOM (Document Object Model)** adalah representasi HTML sebagai pohon objek. Dengan JavaScript, kamu bisa **membaca, mengubah, menambah, atau menghapus** elemen HTML secara dinamis.

---

## Memilih Elemen

```javascript
// Pilih berdasarkan ID
const judul = document.getElementById("judul");

// Pilih berdasarkan class (mengambil semua)
const tombol = document.querySelectorAll(".btn");

// Pilih satu elemen (CSS selector)
const pertama = document.querySelector("p");
const khusus = document.querySelector("#form .input-email");
```

---

## Mengubah Konten

```javascript
const elemen = document.getElementById("output");

// Ubah teks
elemen.textContent = "Teks baru (aman dari XSS)";

// Ubah HTML
elemen.innerHTML = "<strong>Teks tebal</strong>";

// Ubah atribut
const gambar = document.querySelector("img");
gambar.src = "foto-baru.jpg";
gambar.alt = "Deskripsi baru";
```

---

## Mengubah Style

```javascript
const kotak = document.getElementById("kotak");

// Ubah style langsung
kotak.style.backgroundColor = "blue";
kotak.style.width = "200px";
kotak.style.display = "none"; // sembunyikan

// Lebih baik: tambah/hapus class CSS
kotak.classList.add("aktif");
kotak.classList.remove("tersembunyi");
kotak.classList.toggle("gelap");   // tambah kalau tidak ada, hapus kalau ada
```

---

## Event Listener

```javascript
const tombol = document.getElementById("tombol-submit");

// Cara modern (direkomendasikan)
tombol.addEventListener("click", function() {
  alert("Tombol diklik!");
});

// Dengan arrow function
tombol.addEventListener("click", () => {
  console.log("Diklik!");
});

// Event lainnya
document.addEventListener("keydown", (e) => {
  console.log("Tombol keyboard:", e.key);
});

const input = document.getElementById("search");
input.addEventListener("input", (e) => {
  console.log("Nilai sekarang:", e.target.value);
});
```

---

## Contoh Lengkap: Counter

```html
<!-- HTML -->
<div id="app">
  <p>Hitungan: <span id="angka">0</span></p>
  <button id="tambah">+ Tambah</button>
  <button id="kurang">- Kurang</button>
  <button id="reset">Reset</button>
</div>

<script>
  let count = 0;
  const display = document.getElementById("angka");

  document.getElementById("tambah").addEventListener("click", () => {
    count++;
    display.textContent = count;
  });

  document.getElementById("kurang").addEventListener("click", () => {
    count--;
    display.textContent = count;
  });

  document.getElementById("reset").addEventListener("click", () => {
    count = 0;
    display.textContent = count;
  });
</script>
```
