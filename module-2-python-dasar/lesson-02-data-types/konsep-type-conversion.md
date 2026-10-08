## Type Conversion - Ubah Tipe Data

Kadang lu perlu convert tipe data: string → int, int → string, dll.

---

### Kenapa Perlu Type Conversion?

**Skenario 1: Input user**

```python
umur = input("Umur: ")  # Input selalu string!
print(umur + 5)  # ❌ Error: can't add string + int
```

Harus convert dulu:

```python
umur = input("Umur: ")
umur = int(umur)  # Convert string → int
print(umur + 5)  # ✅ Jalan
```

**Skenario 2: Print angka + text**

```python
umur = 25
print("Umur: " + umur)  # ❌ Error: can't concatenate str + int
```

Convert int → string:

```python
umur = 25
print("Umur: " + str(umur))  # ✅ Jalan
```

---

### Built-in Conversion Functions

#### 1. `int()` - Convert ke Integer

```python
# String → Int
umur_str = "25"
umur_int = int(umur_str)
print(umur_int + 5)  # 30

# Float → Int (buang desimal)
harga = 99.99
harga_bulat = int(harga)
print(harga_bulat)  # 99

# Boolean → Int
print(int(True))   # 1
print(int(False))  # 0
```

**Error kalau string bukan angka**:

```python
int("abc")  # ❌ ValueError: invalid literal for int()
```

---

#### 2. `float()` - Convert ke Float

```python
# String → Float
harga = "99.99"
harga_float = float(harga)
print(harga_float + 10)  # 109.99

# Int → Float
umur = 25
umur_float = float(umur)
print(umur_float)  # 25.0
```

---

#### 3. `str()` - Convert ke String

```python
# Int → String
umur = 25
umur_str = str(umur)
print("Umur: " + umur_str)  # "Umur: 25"

# Float → String
harga = 99.99
print("Harga: Rp " + str(harga))  # "Harga: Rp 99.99"

# List → String (jadi representasi text)
buah = ["apel", "jeruk"]
print(str(buah))  # "['apel', 'jeruk']"
```

---

#### 4. `bool()` - Convert ke Boolean

```python
# Angka → Bool (0 = False, selain 0 = True)
print(bool(0))    # False
print(bool(1))    # True
print(bool(-1))   # True
print(bool(100))  # True

# String → Bool (empty string = False, ada isi = True)
print(bool(""))      # False
print(bool("hello")) # True

# List → Bool (empty list = False, ada isi = True)
print(bool([]))      # False
print(bool([1, 2]))  # True
```

---

### Check Tipe Data

Pake `type()`:

```python
umur = 25
nama = "Rafi"
harga = 99.99
aktif = True

print(type(umur))   # <class 'int'>
print(type(nama))   # <class 'str'>
print(type(harga))  # <class 'float'>
print(type(aktif))  # <class 'bool'>
```

**Check tipe tertentu**:

```python
umur = 25

if type(umur) == int:
    print("Ini integer")

# Atau pake isinstance (lebih pythonic)
if isinstance(umur, int):
    print("Ini integer")
```

---

### Contoh Praktis

**Use case 1: Input calculator**

```python
# Input dari user (selalu string)
angka1 = input("Angka 1: ")
angka2 = input("Angka 2: ")

# Convert ke int
angka1 = int(angka1)
angka2 = int(angka2)

# Hitung
hasil = angka1 + angka2
print(f"Hasil: {hasil}")
```

**Use case 2: Parse data CSV**

```python
# Data dari CSV (semua string)
data = "Rafi,25,Jakarta,175.5"

# Split jadi list
parts = data.split(",")  # ['Rafi', '25', 'Jakarta', '175.5']

# Convert tipe yang sesuai
nama = parts[0]           # string
umur = int(parts[1])      # int
kota = parts[2]           # string
tinggi = float(parts[3])  # float

print(f"{nama}, {umur} tahun, tinggi {tinggi} cm")
```

**Use case 3: Format output**

```python
total = 1500000

# Int → String dengan format
total_str = f"Rp {total:,}"
print(total_str)  # Rp 1,500,000

# Atau manual convert
print("Total: Rp " + str(total))
```

---

### Safe Conversion (Avoid Crash)

**Problem**: `int("abc")` → crash

**Solution**: Try-except (nanti di advanced lesson)

Atau check dulu:

```python
input_user = "123"

if input_user.isdigit():
    umur = int(input_user)
    print(f"Umur: {umur}")
else:
    print("Input harus angka")
```

**String methods buat validasi**:

```python
"123".isdigit()     # True (semua digit)
"12.3".isdigit()    # False (ada titik)
"abc".isalpha()     # True (semua huruf)
"abc123".isalnum()  # True (huruf + angka)
```

---

### List/Dict Conversion

#### String → List (split)

```python
text = "apel,jeruk,mangga"
buah = text.split(",")
print(buah)  # ['apel', 'jeruk', 'mangga']
```

#### List → String (join)

```python
buah = ["apel", "jeruk", "mangga"]
text = ", ".join(buah)
print(text)  # "apel, jeruk, mangga"
```

#### Dict → List (keys/values)

```python
user = {"nama": "Rafi", "umur": 25}

keys = list(user.keys())     # ['nama', 'umur']
values = list(user.values()) # ['Rafi', 25]
```

#### List of Lists → Dict

```python
data = [["nama", "Rafi"], ["umur", 25]]
user = dict(data)
print(user)  # {'nama': 'Rafi', 'umur': 25}
```

---

## Kesalahan Umum

**1. Convert string non-angka ke int**

```python
int("abc")  # ❌ ValueError
```

**Fix**: Validasi dulu

```python
if text.isdigit():
    angka = int(text)
```

**2. Lupa convert input**

```python
umur = input("Umur: ")  # String!
if umur >= 18:  # ❌ Compare string sama int
    print("Dewasa")
```

**Fix**:

```python
umur = int(input("Umur: "))  # Convert langsung
if umur >= 18:
    print("Dewasa")
```

**3. Float → Int kehilangan desimal**

```python
harga = 99.99
harga_int = int(harga)
print(harga_int)  # 99 (bukan 100, ga dibulatkan, langsung potong)
```

Kalau mau bulatkan, pake `round()`:

```python
harga = 99.99
harga_bulat = round(harga)
print(harga_bulat)  # 100
```

---

## Rangkuman

| Function | Convert ke | Contoh |
|----------|-----------|--------|
| `int()` | Integer | `int("25")` → `25` |
| `float()` | Float | `float("99.9")` → `99.9` |
| `str()` | String | `str(25)` → `"25"` |
| `bool()` | Boolean | `bool(1)` → `True` |
| `type()` | Check tipe | `type(25)` → `<class 'int'>` |

**Rule penting**: Input dari user **selalu string**, harus convert kalau mau operasi matematika.

---

Next: **Exercises** - praktek manipulasi data types.
