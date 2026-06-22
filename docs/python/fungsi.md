---
title: Fungsi
layout: default
parent: Python
nav_order: 3
---

# Python — Fungsi
{: .no_toc }

<details open markdown="block">
<summary>Daftar Isi</summary>
{: .text-delta }
1. TOC
{:toc}
</details>

---

## Apa itu Fungsi?

Fungsi adalah **blok kode yang bisa dipakai ulang**. Daripada menulis kode yang sama berkali-kali, simpan di fungsi dan panggil kapan pun dibutuhkan.

```python
# Mendefinisikan fungsi
def sapa():
    print("Halo! Selamat datang di Bale Tech!")

# Memanggil fungsi
sapa()  # Halo! Selamat datang di Bale Tech!
sapa()  # bisa dipanggil berkali-kali
```

---

## Fungsi dengan Parameter

```python
def sapa_nama(nama):
    print(f"Halo, {nama}! Selamat belajar Python!")

sapa_nama("Ade")    # Halo, Ade! Selamat belajar Python!
sapa_nama("Budi")   # Halo, Budi! Selamat belajar Python!
```

---

## Fungsi dengan Return Value

```python
def tambah(a, b):
    return a + b

hasil = tambah(5, 3)
print(hasil)  # 8

# Langsung dipakai
print(tambah(10, 20))  # 30
```

---

## Parameter Default

```python
def sapa(nama, sapaan="Halo"):
    print(f"{sapaan}, {nama}!")

sapa("Ade")           # Halo, Ade!
sapa("Budi", "Selamat pagi")  # Selamat pagi, Budi!
```

---

## Lambda (Fungsi Singkat)

```python
# Fungsi biasa
def kuadrat(x):
    return x ** 2

# Lambda (versi singkat)
kuadrat = lambda x: x ** 2

print(kuadrat(5))   # 25
print(kuadrat(10))  # 100
```

---

## Contoh Nyata

```python
def hitung_luas_persegi_panjang(panjang, lebar):
    """Menghitung luas persegi panjang."""
    luas = panjang * lebar
    return luas

def hitung_keliling(panjang, lebar):
    """Menghitung keliling persegi panjang."""
    keliling = 2 * (panjang + lebar)
    return keliling

# Gunakan fungsi
p = 10
l = 5
print(f"Luas: {hitung_luas_persegi_panjang(p, l)} cm²")     # Luas: 50 cm²
print(f"Keliling: {hitung_keliling(p, l)} cm")               # Keliling: 30 cm
```
