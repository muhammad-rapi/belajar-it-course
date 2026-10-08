## String Operations

String = text. Python punya banyak built-in method buat manipulasi string.

---

### Bikin String

```python
# Single quote atau double quote, sama aja
nama = "Rafi"
kota = 'Jakarta'

# Multi-line string pake triple quote
bio = """
Nama: Rafi
Kota: Jakarta
Hobi: Coding
"""
```

---

### String Methods (Built-in Functions)

#### 1. Uppercase / Lowercase

```python
nama = "rafi maulana"

print(nama.upper())       # RAFI MAULANA
print(nama.lower())       # rafi maulana
print(nama.capitalize())  # Rafi maulana
print(nama.title())       # Rafi Maulana (tiap kata capital)
```

**Use case**: Validasi input user (misal: "Jakarta", "jakarta", "JAKARTA" → semua jadi lowercase biar gampang compare).

---

#### 2. Strip (Buang Spasi)

```python
nama = "  Rafi  "  # Ada spasi di kiri-kanan

print(nama.strip())   # "Rafi" (buang spasi kiri-kanan)
print(nama.lstrip())  # "Rafi  " (buang spasi kiri)
print(nama.rstrip())  # "  Rafi" (buang spasi kanan)
```

**Use case**: Input dari user sering ada spasi ga sengaja.

---

#### 3. Replace (Ganti Text)

```python
kalimat = "Aku suka apel"

print(kalimat.replace("apel", "mangga"))  # "Aku suka mangga"
print(kalimat.replace("suka", "benci"))   # "Aku benci apel"
```

**Use case**: Sensor kata, fix typo massal.

---

#### 4. Split (Pecah String jadi List)

```python
nama_lengkap = "Rafi Maulana Hidayat"
nama_list = nama_lengkap.split(" ")  # Pecah pake spasi

print(nama_list)  # ['Rafi', 'Maulana', 'Hidayat']
print(nama_list[0])  # Rafi
print(nama_list[1])  # Maulana
```

**Use case**: Parse data CSV, pisah first name & last name.

---

#### 5. Join (Gabung List jadi String)

```python
kata = ["Aku", "suka", "Python"]
kalimat = " ".join(kata)  # Gabung pake spasi

print(kalimat)  # "Aku suka Python"

# Gabung pake karakter lain
print("-".join(kata))  # "Aku-suka-Python"
print("_".join(kata))  # "Aku_suka_Python"
```

**Use case**: Bikin sentence dari list kata.

---

#### 6. Find / Index

```python
kalimat = "Aku suka Python"

print(kalimat.find("suka"))     # 4 (index dimulai dari 0)
print(kalimat.find("apel"))     # -1 (ga ketemu)
print("Python" in kalimat)      # True
print("Java" in kalimat)        # False
```

**Use case**: Cek keyword ada ga dalam text.

---

### String Slicing (Potong String)

```python
text = "Python Programming"

print(text[0])      # P (karakter pertama)
print(text[-1])     # g (karakter terakhir)
print(text[0:6])    # Python (index 0 sampai 5)
print(text[7:])     # Programming (index 7 sampai akhir)
print(text[:6])     # Python (awal sampai index 5)
```

**Syntax**: `text[start:end]` (end tidak termasuk)

**Contoh praktis**:

```python
email = "rafi@gmail.com"
username = email.split("@")[0]  # rafi
domain = email.split("@")[1]    # gmail.com

print(f"Username: {username}")
print(f"Domain: {domain}")
```

---

### String Formatting (F-String)

```python
nama = "Rafi"
umur = 25

# ❌ Cara lama (concatenation)
pesan = "Nama: " + nama + ", Umur: " + str(umur)

# ✅ F-string (Python 3.6+)
pesan = f"Nama: {nama}, Umur: {umur}"
print(pesan)  # Nama: Rafi, Umur: 25

# Bisa operasi langsung dalam {}
print(f"Tahun depan umur {nama} adalah {umur + 1}")
# Output: Tahun depan umur Rafi adalah 26
```

**Format angka**:

```python
harga = 1500000

print(f"Harga: Rp {harga:,}")      # Rp 1,500,000
print(f"Harga: Rp {harga:,.2f}")   # Rp 1,500,000.00

pi = 3.14159
print(f"Pi: {pi:.2f}")  # Pi: 3.14 (2 desimal)
```

---

### String adalah Immutable

String **ga bisa diubah** setelah dibuat. Method kayak `.replace()` **return string baru**, bukan ubah yang lama.

```python
nama = "Rafi"
nama.upper()  # ❌ Ini ga ngubah `nama`
print(nama)   # Output: Rafi (masih lowercase)

# ✅ Harus assign ulang
nama = nama.upper()
print(nama)  # Output: RAFI
```

---

## Rangkuman String Methods

| Method | Fungsi | Contoh |
|--------|--------|--------|
| `.upper()` | Uppercase semua | `"rafi".upper()` → `"RAFI"` |
| `.lower()` | Lowercase semua | `"RAFI".lower()` → `"rafi"` |
| `.strip()` | Buang spasi kiri-kanan | `"  hi  ".strip()` → `"hi"` |
| `.replace(a, b)` | Ganti `a` jadi `b` | `"aku".replace("a", "e")` → `"eku"` |
| `.split(sep)` | Pecah jadi list | `"a b".split(" ")` → `['a', 'b']` |
| `sep.join(list)` | Gabung list | `" ".join(['a', 'b'])` → `"a b"` |
| `.find(sub)` | Index substring | `"hello".find("ll")` → `2` |
| `[start:end]` | Slice | `"Python"[0:3]` → `"Pyt"` |

Next: **Lists** - cara simpen banyak data sekaligus.
