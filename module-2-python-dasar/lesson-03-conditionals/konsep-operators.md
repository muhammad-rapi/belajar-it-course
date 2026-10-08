## Comparison & Logic Operators

Sampe sekarang lu udah pake operator kayak `>=`, `==`. Sekarang kita bahas **semua operator** + cara **combine multiple kondisi**.

---

### Comparison Operators (Review)

| Operator | Arti | Contoh | Hasil |
|----------|------|--------|-------|
| `==` | Sama dengan | `5 == 5` | `True` |
| `!=` | Tidak sama dengan | `5 != 3` | `True` |
| `>` | Lebih besar | `10 > 5` | `True` |
| `<` | Lebih kecil | `3 < 5` | `True` |
| `>=` | Lebih besar atau sama | `5 >= 5` | `True` |
| `<=` | Lebih kecil atau sama | `4 <= 5` | `True` |

---

### Logic Operators

Combine multiple kondisi:

#### 1. `and` - Semua harus True

```python
umur = 25
punya_sim = True

if umur >= 17 and punya_sim:
    print("Boleh nyetir")
```

**Truth table**:
- `True and True` = `True`
- `True and False` = `False`
- `False and True` = `False`
- `False and False` = `False`

**Contoh**:

```python
nilai = 85
kehadiran = 90

if nilai >= 70 and kehadiran >= 80:
    print("Lulus")
else:
    print("Tidak lulus")
```

Output: `Lulus` (karena 85 >= 70 **dan** 90 >= 80)

---

#### 2. `or` - Salah satu True = True

```python
is_member = True
total_belanja = 150000

if is_member or total_belanja >= 200000:
    print("Dapat diskon")
```

**Truth table**:
- `True or True` = `True`
- `True or False` = `True`
- `False or True` = `True`
- `False or False` = `False`

**Contoh**:

```python
metode_bayar = "gopay"

if metode_bayar == "gopay" or metode_bayar == "ovo":
    print("Dapat cashback 10%")
```

---

#### 3. `not` - Balik nilai

```python
sudah_login = False

if not sudah_login:
    print("Silakan login dulu")
```

**Truth table**:
- `not True` = `False`
- `not False` = `True`

**Contoh**:

```python
file_exists = False

if not file_exists:
    print("File tidak ditemukan")
```

---

### Combine Multiple Logic Operators

```python
umur = 25
punya_sim = True
punya_mobil = False

if umur >= 17 and punya_sim and punya_mobil:
    print("Boleh nyetir mobil sendiri")
elif umur >= 17 and punya_sim:
    print("Boleh nyetir, tapi harus pinjem mobil")
else:
    print("Belum boleh nyetir")
```

---

### Operator Precedence (Prioritas)

**Urutan evaluasi**:
1. `not`
2. `and`
3. `or`

**Contoh**:

```python
a = True
b = False
c = True

# not diproses dulu, baru and, baru or
result = a or b and not c
# = a or (b and (not c))
# = True or (False and False)
# = True or False
# = True
```

**Best practice**: Pake kurung biar jelas

```python
result = a or (b and (not c))  # Lebih jelas
```

---

### `in` Operator - Check Membership

```python
buah = ["apel", "jeruk", "mangga"]

if "apel" in buah:
    print("Ada apel")

if "pisang" not in buah:
    print("Ga ada pisang")
```

**Buat string**:

```python
email = "rafi@gmail.com"

if "@" in email and "." in email:
    print("Email valid")
else:
    print("Email tidak valid")
```

---

### Chained Comparison

Python bisa chain comparison:

**Cara biasa**:

```python
umur = 25

if umur >= 18 and umur <= 60:
    print("Dewasa")
```

**Chained** (lebih pendek):

```python
umur = 25

if 18 <= umur <= 60:
    print("Dewasa")
```

**Contoh lain**:

```python
nilai = 85

if 80 <= nilai < 90:
    print("Grade B")
```

---

## Contoh Praktis

**Use case 1: Validasi registrasi**

```python
username = "rafi_dev"
password = "secret123"
umur = 20

if len(username) >= 5 and len(password) >= 8 and umur >= 13:
    print("Registrasi berhasil")
else:
    print("Validasi gagal:")
    if len(username) < 5:
        print("- Username min 5 karakter")
    if len(password) < 8:
        print("- Password min 8 karakter")
    if umur < 13:
        print("- Umur min 13 tahun")
```

**Use case 2: Promo belanja**

```python
total = 250000
is_member = True
metode_bayar = "gopay"

diskon = 0

if is_member and total >= 200000:
    diskon += 10  # Member + min belanja
if metode_bayar == "gopay" or metode_bayar == "ovo":
    diskon += 5   # Cashback ewallet

print(f"Total: Rp {total:,}")
print(f"Diskon: {diskon}%")
print(f"Bayar: Rp {int(total * (1 - diskon/100)):,}")
```

---

## Kesalahan Umum

**1. Lupa operator di multiple checks**

```python
# ❌ Salah (Python bingung)
if umur >= 18 and < 60:
    print("Dewasa")
```

**Fix**:

```python
# ✅ Benar
if umur >= 18 and umur < 60:
    print("Dewasa")

# Atau pake chained
if 18 <= umur < 60:
    print("Dewasa")
```

**2. Confuse `and` vs `or`**

Mau **keduanya harus True**? Pake `and`.  
Mau **salah satu True**? Pake `or`.

```python
# Lulus kalau nilai >= 70 DAN kehadiran >= 80
if nilai >= 70 and kehadiran >= 80:
    print("Lulus")

# Dapat diskon kalau member ATAU belanja >= 200k
if is_member or total >= 200000:
    print("Dapat diskon")
```

**3. Typo operator**

```python
if umur = 18:  # ❌ Assignment, bukan comparison
if umur == 18: # ✅ Comparison
```

---

## Rangkuman

| Operator | Fungsi | Contoh |
|----------|--------|--------|
| `and` | Semua harus True | `a and b` |
| `or` | Salah satu True | `a or b` |
| `not` | Balik nilai | `not a` |
| `in` | Check membership | `"x" in list` |
| Chained | Range check | `18 <= x <= 60` |

---

Next: **Exercises** - praktek bikin conditional logic.
