---
title: Sintaks Dasar
layout: default
parent: Python
nav_order: 1
---

# Python — Sintaks Dasar
{: .no_toc }

<details open markdown="block">
<summary>Daftar Isi</summary>
{: .text-delta }
1. TOC
{:toc}
</details>

---

## Hello World

Program pertama di Python sangat simpel:

```python
print("Hello, World!")
```

**Output:**
```
Hello, World!
```

---

## Komentar

Komentar adalah catatan yang tidak dieksekusi Python:

```python
# Ini komentar satu baris

"""
Ini komentar
beberapa baris
(sebenarnya ini string, tapi sering dipakai sebagai komentar)
"""
```

---

## Indentasi (Penting!)

Python menggunakan **indentasi** (spasi/tab) untuk mengelompokkan kode. Ini berbeda dari bahasa lain yang pakai `{}`.

```python
# BENAR ✅
if True:
    print("Ini di dalam if")
    print("Ini juga")

# SALAH ❌ — akan error!
if True:
print("Lupa indentasi")
```

{: .warning }
> Selalu konsisten: pakai **4 spasi** per level indentasi.

---

## Input dari User

```python
nama = input("Masukkan nama kamu: ")
print("Halo,", nama)
```

**Output:**
```
Masukkan nama kamu: Ade
Halo, Ade
```

---

## Operasi Matematika

```python
a = 10
b = 3

print(a + b)   # 13  → Penjumlahan
print(a - b)   # 7   → Pengurangan
print(a * b)   # 30  → Perkalian
print(a / b)   # 3.333... → Pembagian
print(a // b)  # 3   → Pembagian bulat
print(a % b)   # 1   → Sisa bagi (modulo)
print(a ** b)  # 1000 → Pangkat
```

---

## Tipe Data Dasar

```python
# Integer (bilangan bulat)
umur = 25

# Float (bilangan desimal)
tinggi = 1.75

# String (teks)
nama = "Putra"

# Boolean (benar/salah)
sudah_makan = True
lapar = False

# Cek tipe data
print(type(umur))    # <class 'int'>
print(type(tinggi))  # <class 'float'>
print(type(nama))    # <class 'str'>
```

---

## Selanjutnya

👉 [Variabel & Tipe Data](/bale-tech-docs/docs/python/variabel)
