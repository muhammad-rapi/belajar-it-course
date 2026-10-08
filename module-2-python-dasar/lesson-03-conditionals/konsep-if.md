## If Statement - Keputusan Dasar

Syntax paling simple: **"kalau kondisi terpenuhi, jalankan code ini"**.

---

### Syntax

```python
if kondisi:
    # code yang jalan kalau kondisi True
    print("Kondisi terpenuhi")
```

**Aturan penting**:
- Kondisi diakhiri `:` (titik dua)
- Code di dalamnya **harus indent** (4 spasi atau 1 tab)
- Kalau kondisi `True` → code jalan
- Kalau kondisi `False` → code di-skip

---

### Contoh 1: Simple Check

```python
umur = 20

if umur >= 18:
    print("Kamu sudah dewasa")
    print("Boleh buat KTP")
```

Output:
```
Kamu sudah dewasa
Boleh buat KTP
```

Karena `20 >= 18` itu `True`, code di dalamnya jalan.

**Coba ubah**:

```python
umur = 15

if umur >= 18:
    print("Kamu sudah dewasa")
    print("Boleh buat KTP")
```

Output: **(kosong, ga ada output)**

Karena `15 >= 18` itu `False`, code di-skip.

---

### Contoh 2: Password Check

```python
password = "rahasia123"
input_user = "rahasia123"

if input_user == password:
    print("Login berhasil!")
    print("Selamat datang")
```

Output:
```
Login berhasil!
Selamat datang
```

**Note**: `==` buat compare (beda sama `=` yang buat assign).

---

### Indent itu WAJIB

Python pake indent buat tau mana code yang ada di dalam `if`.

**❌ Salah (ga ada indent)**:

```python
if umur >= 18:
print("Dewasa")  # IndentationError
```

**✅ Benar (ada indent)**:

```python
if umur >= 18:
    print("Dewasa")  # Indent 4 spasi
```

---

### Multiple Statements

Lu bisa punya banyak baris di dalam `if`:

```python
saldo = 1000000

if saldo >= 500000:
    print("Saldo mencukupi")
    print("Transaksi diproses")
    saldo = saldo - 500000
    print(f"Sisa saldo: {saldo}")
```

Output:
```
Saldo mencukupi
Transaksi diproses
Sisa saldo: 500000
```

Semua baris yang indent jalan kalau kondisi `True`.

---

### Comparison Operators

Operator buat compare nilai:

| Operator | Arti | Contoh | Hasil |
|----------|------|--------|-------|
| `==` | Sama dengan | `5 == 5` | `True` |
| `!=` | Tidak sama dengan | `5 != 3` | `True` |
| `>` | Lebih besar | `10 > 5` | `True` |
| `<` | Lebih kecil | `3 < 5` | `True` |
| `>=` | Lebih besar atau sama | `5 >= 5` | `True` |
| `<=` | Lebih kecil atau sama | `4 <= 5` | `True` |

**Contoh**:

```python
nilai = 85

if nilai > 80:
    print("Nilai bagus!")

if nilai == 100:
    print("Perfect score!")  # Ga jalan karena 85 != 100

if nilai != 0:
    print("Kamu sudah ujian")  # Jalan karena 85 != 0
```

Output:
```
Nilai bagus!
Kamu sudah ujian
```

---

### String Comparison

Bisa compare string juga:

```python
nama = "Rafi"

if nama == "Rafi":
    print("Halo Rafi!")

# Case-sensitive!
if nama == "rafi":
    print("Ini ga jalan")  # Ga jalan karena "Rafi" != "rafi"

# Compare lowercase
if nama.lower() == "rafi":
    print("Ini jalan!")  # Jalan
```

---

### Boolean Variable

Bisa langsung pake boolean:

```python
sudah_login = True

if sudah_login:
    print("Welcome back!")

# Sama aja dengan:
if sudah_login == True:
    print("Welcome back!")
```

Tapi cara pertama lebih pythonic (lebih singkat).

---

### Nested If (If di dalam If)

```python
umur = 25
punya_sim = True

if umur >= 17:
    print("Umur cukup")
    if punya_sim:
        print("Boleh nyetir")
```

Output:
```
Umur cukup
Boleh nyetir
```

**Note**: Nested if butuh double indent (8 spasi).

---

## Contoh Praktis

**Use case 1: Diskon member**

```python
is_member = True
total_belanja = 150000

if is_member:
    diskon = total_belanja * 0.1
    total_belanja = total_belanja - diskon
    print(f"Dapat diskon! Total: Rp {int(total_belanja):,}")
```

**Use case 2: Validasi input**

```python
username = "rafi_dev"

if len(username) < 5:
    print("Username terlalu pendek (min 5 karakter)")

if " " in username:
    print("Username ga boleh ada spasi")
```

---

## Kesalahan Umum

**1. Lupa titik dua (:)**

```python
if umur >= 18  # ❌ SyntaxError
    print("Dewasa")
```

**Fix**: Tambahin `:`

```python
if umur >= 18:  # ✅
    print("Dewasa")
```

**2. Pakai `=` bukan `==`**

```python
if nama = "Rafi":  # ❌ SyntaxError (assignment, bukan comparison)
```

**Fix**:

```python
if nama == "Rafi":  # ✅
```

**3. Lupa indent**

```python
if umur >= 18:
print("Dewasa")  # ❌ IndentationError
```

**Fix**: Indent 4 spasi

```python
if umur >= 18:
    print("Dewasa")  # ✅
```

---

Next: **If-Else** - handle "kalau ga, lakukan ini".
