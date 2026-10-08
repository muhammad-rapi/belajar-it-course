## Kenapa Tipe Data Penting?

Di Lesson 1, lu udah bikin variable:

```python
nama = "Rafi"
umur = 25
```

`nama` itu **string** (text), `umur` itu **integer** (angka). Kenapa bedain tipe? Karena **operasi yang bisa dilakuin beda**.

---

### Masalah yang Sering Muncul

**Skenario 1: Input dari user**

```python
# User ketik umur
umur_input = "25"  # Ini STRING (dari keyboard)
umur_tahun_depan = umur_input + 1  # ❌ Error!
```

Error: `TypeError: can only concatenate str (not "int") to str`

Python ga bisa tambah string + angka. Lu harus convert dulu.

**Skenario 2: Simpen data banyak**

```python
# Kalau lu punya 100 nama, apa bikin 100 variable?
nama1 = "Rafi"
nama2 = "Budi"
nama3 = "Siti"
# ... nama100 = "Andi"  ??? Ribet banget!
```

Solusi: **List** - simpen ratusan item dalam 1 variable.

**Skenario 3: Data terstruktur**

```python
# Info user: nama, umur, kota
# Kalau pake variable terpisah:
user_nama = "Rafi"
user_umur = 25
user_kota = "Jakarta"
```

Ribet kalau data bertambah atau mau passing data ke function. Solusi: **Dictionary** - simpen data pake key-value.

---

## Apa yang Lu Bakal Pelajari

Abis lesson ini, lu bisa:
- Manipulasi string (uppercase, lowercase, slice, replace)
- Simpen dan akses data dalam list
- Bikin dictionary buat data terstruktur
- Convert antar tipe data (string ↔ int ↔ float)
- Paham error type mismatch dan cara fixnya

---

## 4 Tipe Data Utama Python

```python
# 1. String - text
nama = "Rafi"
alamat = 'Jl. Sudirman No. 123'

# 2. Integer - angka bulat
umur = 25
jumlah = 100

# 3. Float - angka desimal
tinggi = 175.5
harga = 99.99

# 4. Boolean - True/False
sudah_login = True
punya_akun = False
```

Plus 2 tipe data collection:

```python
# 5. List - array, ordered
buah = ["apel", "jeruk", "mangga"]

# 6. Dictionary - object, key-value
user = {
    "nama": "Rafi",
    "umur": 25,
    "kota": "Jakarta"
}
```

Lesson ini fokus ke **String, List, Dictionary** karena paling sering dipake.

---

Ready? Mulai dari String Operations.
