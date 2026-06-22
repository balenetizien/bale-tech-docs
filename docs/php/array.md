---
title: Array
layout: default
parent: PHP
nav_order: 2
---

# PHP — Array
{: .no_toc }

<details open markdown="block">
<summary>Daftar Isi</summary>
{: .text-delta }
1. TOC
{:toc}
</details>

---

## Array Indexed

Array indexed menyimpan data dengan urutan (index dimulai dari 0):

```php
<?php
$buah = ["apel", "mangga", "jeruk", "pisang"];

echo $buah[0];   // apel
echo $buah[2];   // jeruk

// Menambah elemen
$buah[] = "anggur";           // tambah di akhir
array_push($buah, "nanas");  // cara lain

// Jumlah elemen
echo count($buah);  // 6

// Looping
foreach ($buah as $item) {
    echo $item . "<br>";
}
?>
```

---

## Array Associative

Array associative menggunakan **key** (nama) bukan angka:

```php
<?php
$mahasiswa = [
    "nama"  => "Putra Ade",
    "umur"  => 25,
    "kota"  => "Bandung",
    "aktif" => true
];

echo $mahasiswa["nama"];   // Putra Ade
echo $mahasiswa["kota"];   // Bandung

// Menambah/mengubah
$mahasiswa["email"] = "ade@email.com";

// Looping
foreach ($mahasiswa as $key => $value) {
    echo "$key: $value<br>";
}
?>
```

---

## Fungsi Array yang Sering Dipakai

```php
<?php
$angka = [3, 1, 4, 1, 5, 9, 2, 6];

sort($angka);              // Urutkan ascending
print_r($angka);           // [1, 1, 2, 3, 4, 5, 6, 9]

rsort($angka);             // Urutkan descending

$unik = array_unique([1, 2, 2, 3, 3, 3]);  // Hapus duplikat
print_r($unik);            // [1, 2, 3]

$posisi = array_search(4, $angka);  // Cari nilai, return index
echo in_array(5, $angka) ? "Ada" : "Tidak ada";  // Ada

// Slice (ambil sebagian)
$tiga_pertama = array_slice($angka, 0, 3);
?>
```
