---
title: Sintaks Dasar
layout: default
parent: JavaScript
nav_order: 1
---

# JavaScript — Sintaks Dasar
{: .no_toc }

<details open markdown="block">
<summary>Daftar Isi</summary>
{: .text-delta }
1. TOC
{:toc}
</details>

---

## Cara Menyisipkan JavaScript ke HTML

```html
<!-- Cara 1: Di dalam tag <script> -->
<script>
  console.log("Hello dari JavaScript!");
</script>

<!-- Cara 2: File terpisah (direkomendasikan) -->
<script src="script.js"></script>
```

{: .tip }
> Taruh tag `<script>` sebelum `</body>` agar HTML dimuat lebih dulu.

---

## Output

```javascript
// Ke console browser (buka DevTools → Console)
console.log("Halo, Dunia!");
console.log(42);
console.log(true);

// Alert (popup)
alert("Ini adalah pesan popup!");

// Ke HTML
document.getElementById("output").innerHTML = "Teks baru!";
```

---

## Variabel

```javascript
// var — cara lama (hindari)
var nama = "Ade";

// let — untuk variabel yang bisa berubah
let umur = 25;
umur = 26;  // ✅ bisa diubah

// const — untuk nilai yang tidak berubah
const PI = 3.14159;
// PI = 3;  // ❌ error!
```

{: .important }
> Selalu pakai `const` dulu. Kalau perlu diubah, baru ganti ke `let`. Hindari `var`.

---

## Tipe Data

```javascript
let teks    = "Halo";           // String
let angka   = 42;               // Number
let desimal = 3.14;             // Number (sama, tidak ada int/float terpisah)
let benar   = true;             // Boolean
let kosong  = null;             // Null
let belum   = undefined;        // Undefined

// Array
let buah = ["apel", "mangga", "jeruk"];

// Object
let orang = {
  nama: "Putra Ade",
  umur: 25,
  kota: "Bandung"
};

// Cek tipe
console.log(typeof teks);    // "string"
console.log(typeof angka);   // "number"
console.log(typeof benar);   // "boolean"
```

---

## Operasi dan Kondisi

```javascript
// Matematika
let a = 10, b = 3;
console.log(a + b);   // 13
console.log(a ** b);  // 1000

// Perbandingan — SELALU pakai === (strict)
console.log(5 === 5);   // true
console.log(5 === "5"); // false (tipe berbeda)
console.log(5 == "5");  // true (jangan pakai ini!)

// Kondisi
let nilai = 80;
if (nilai >= 90) {
  console.log("A");
} else if (nilai >= 75) {
  console.log("B");  // ini yang tercetak
} else {
  console.log("C");
}

// Ternary (kondisi singkat)
let status = nilai >= 75 ? "Lulus" : "Tidak Lulus";
console.log(status);  // "Lulus"
```

---

## Loop

```javascript
// For loop
for (let i = 1; i <= 5; i++) {
  console.log(`Iterasi ke-${i}`);
}

// While loop
let hitungan = 0;
while (hitungan < 3) {
  console.log(hitungan);
  hitungan++;
}

// forEach untuk array
const buah = ["apel", "mangga", "jeruk"];
buah.forEach(item => {
  console.log(item);
});
```
