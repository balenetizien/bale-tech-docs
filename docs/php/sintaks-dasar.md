---
title: Sintaks Dasar
layout: default
parent: PHP
nav_order: 1
---

# PHP — Sintaks Dasar
{: .no_toc }

<details open markdown="block">
<summary>Daftar Isi</summary>
{: .text-delta }
1. TOC
{:toc}
</details>

---

## Struktur File PHP

File PHP diawali dan diakhiri dengan tag khusus:

```php
<?php
// Kode PHP ditulis di sini
echo "Hello, World!";
?>
```

{: .note }
> Jika file hanya berisi PHP (tanpa HTML), kamu bisa tidak menutup tag `?>` di akhir file. Ini adalah praktik yang dianjurkan.

---

## Output / Menampilkan Teks

```php
<?php
// Cara 1: echo (paling umum)
echo "Halo, Dunia!";

// Cara 2: print
print "Halo juga!";

// Cara 3: dengan HTML
echo "<h1>Judul Besar</h1>";
echo "<p>Paragraf biasa.</p>";
?>
```

---

## Komentar

```php
<?php
// Komentar satu baris

# Komentar satu baris (cara lain)

/*
  Komentar
  beberapa baris
*/
?>
```

---

## Variabel

```php
<?php
// Variabel selalu dimulai dengan $
$nama = "Putra Ade";
$umur = 25;
$tinggi = 1.75;
$aktif = true;

echo $nama;          // Putra Ade
echo "<br>";
echo "Umur: $umur";  // Umur: 25
?>
```

{: .important }
> Variabel PHP **selalu diawali dengan `$`** dan **case-sensitive** (`$nama` ≠ `$Nama`).

---

## Tipe Data

```php
<?php
$string  = "Teks biasa";          // String
$integer = 42;                    // Integer
$float   = 3.14;                  // Float
$boolean = true;                  // Boolean
$null    = null;                  // Null
$array   = ["apel", "mangga"];    // Array

// Cek tipe data
var_dump($integer);  // int(42)
var_dump($boolean);  // bool(true)
?>
```

---

## Operasi Matematika

```php
<?php
$a = 10;
$b = 3;

echo $a + $b;   // 13
echo $a - $b;   // 7
echo $a * $b;   // 30
echo $a / $b;   // 3.333...
echo $a % $b;   // 1 (modulo)
echo $a ** $b;  // 1000 (pangkat)

// Shorthand
$a += 5;   // sama dengan $a = $a + 5
$a -= 2;   // sama dengan $a = $a - 2
$a *= 3;   // sama dengan $a = $a * 3
?>
```

---

## String

```php
<?php
$nama = "Putra Ade";
$kota = "Bandung";

// Penggabungan string dengan titik (.)
echo $nama . " dari " . $kota;  // Putra Ade dari Bandung

// String interpolation (dalam double quote)
echo "Halo, $nama!";            // Halo, Putra Ade!

// Fungsi string berguna
echo strlen($nama);             // 9 (panjang)
echo strtoupper($nama);         // PUTRA ADE
echo strtolower($nama);         // putra ade
echo str_replace("Ade", "Budi", $nama); // Putra Budi
?>
```

---

## If / Else

```php
<?php
$nilai = 75;

if ($nilai >= 90) {
    echo "Nilai A — Sangat Bagus!";
} elseif ($nilai >= 75) {
    echo "Nilai B — Bagus!";
} elseif ($nilai >= 60) {
    echo "Nilai C — Cukup";
} else {
    echo "Nilai D — Perlu Belajar Lebih";
}
// Output: Nilai B — Bagus!
?>
```
