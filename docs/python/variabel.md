---
title: Variabel & Tipe Data
layout: default
parent: Python
nav_order: 2
---

# Python — Variabel & Tipe Data
{: .no_toc }

<details open markdown="block">
<summary>Daftar Isi</summary>
{: .text-delta }
1. TOC
{:toc}
</details>

---

## Apa itu Variabel?

Variabel adalah **kotak penyimpan data**. Kamu bisa simpan angka, teks, atau data lain di dalamnya.

```python
# Membuat variabel
nama = "Ade"
umur = 25
tinggi = 1.75
aktif = True
```

---

## Aturan Nama Variabel

```python
# ✅ BOLEH
nama_lengkap = "Putra Ade"
nilai1 = 90
_private = "rahasia"
namaUser = "Ade"       # camelCase

# ❌ TIDAK BOLEH
1nama = "error"        # tidak boleh mulai angka
nama-lengkap = "error" # tidak boleh pakai tanda minus
class = "error"        # tidak boleh pakai keyword Python
```

---

## String (Teks)

```python
# Membuat string
nama = "Putra Ade Novit"
kota = 'Bandung'       # bisa pakai tanda kutip tunggal atau ganda
bio = """Ini adalah
teks panjang
beberapa baris"""

# Operasi string
print(len(nama))           # 14 → panjang string
print(nama.upper())        # PUTRA ADE NOVIT
print(nama.lower())        # putra ade novit
print(nama.split(" "))     # ['Putra', 'Ade', 'Novit']

# String formatting (f-string) — cara modern
umur = 25
print(f"Nama saya {nama}, umur {umur} tahun")
```

---

## Integer & Float

```python
# Integer
x = 100
y = -50
z = 0

# Float
pi = 3.14159
suhu = -12.5

# Konversi
angka_str = "42"
angka_int = int(angka_str)    # string → integer
angka_float = float(angka_str) # string → float
kembali_str = str(angka_int)   # integer → string
```

---

## Boolean

```python
benar = True
salah = False

# Operasi logika
print(True and False)  # False
print(True or False)   # True
print(not True)        # False

# Perbandingan menghasilkan Boolean
print(5 > 3)    # True
print(5 < 3)    # False
print(5 == 5)   # True
print(5 != 3)   # True
```

---

## List (Daftar)

```python
# Membuat list
buah = ["apel", "mangga", "jeruk"]
angka = [1, 2, 3, 4, 5]
campuran = ["Ade", 25, True, 1.75]

# Mengakses elemen (index mulai dari 0)
print(buah[0])   # apel
print(buah[-1])  # jeruk (dari belakang)

# Mengubah elemen
buah[1] = "pisang"
print(buah)  # ['apel', 'pisang', 'jeruk']

# Menambah elemen
buah.append("anggur")
print(buah)  # ['apel', 'pisang', 'jeruk', 'anggur']

# Panjang list
print(len(buah))  # 4
```

---

## Dictionary (Kamus)

```python
# Membuat dictionary
mahasiswa = {
    "nama": "Putra Ade",
    "umur": 25,
    "kota": "Bandung",
    "aktif": True
}

# Mengakses nilai
print(mahasiswa["nama"])   # Putra Ade
print(mahasiswa.get("umur"))  # 25

# Menambah/mengubah
mahasiswa["email"] = "ade@email.com"

# Looping
for kunci, nilai in mahasiswa.items():
    print(f"{kunci}: {nilai}")
```
