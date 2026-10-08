## If-Else - Dua Pilihan

`if` sendirian cuma handle kondisi `True`. Kalau `False`, ga ada yang jalan.

`if-else` = **dua pilihan**: "kalau True lakukan A, kalau False lakukan B".

---

### Syntax

```python
if kondisi:
    # Jalan kalau True
    print("Kondisi True")
else:
    # Jalan kalau False
    print("Kondisi False")
```

---

### Contoh 1: Umur

```python
umur = 15

if umur >= 18:
    print("Sudah dewasa")
else:
    print("Belum dewasa")
```

Output: `Belum dewasa`

**Ubah jadi 20**:

```python
umur = 20

if umur >= 18:
    print("Sudah dewasa")
else:
    print("Belum dewasa")
```

Output: `Sudah dewasa`

Salah satu **pasti jalan** (antara `if` atau `else`).

---

### Contoh 2: Login

```python
password_benar = "secret123"
input_user = "salah"

if input_user == password_benar:
    print("Login berhasil!")
else:
    print("Password salah, coba lagi")
```

Output: `Password salah, coba lagi`

---

### Contoh 3: Ganjil/Genap

```python
angka = 7

if angka % 2 == 0:
    print("Genap")
else:
    print("Ganjil")
```

Output: `Ganjil`

**Note**: `%` (modulo) = sisa bagi. `7 % 2` = 1 (sisa 1), jadi ganjil.

---

### Multiple Statements di Else

```python
saldo = 300000
tarik = 500000

if saldo >= tarik:
    print("Transaksi berhasil")
    saldo = saldo - tarik
    print(f"Sisa saldo: {saldo}")
else:
    print("Saldo tidak cukup")
    print("Silakan isi saldo atau tarik jumlah lebih kecil")
```

Output:
```
Saldo tidak cukup
Silakan isi saldo atau tarik jumlah lebih kecil
```

---

### Return Early Pattern

Kadang lu bisa skip `else` dengan return/exit lebih awal:

**Tanpa early return (pake else)**:

```python
umur = 15

if umur >= 18:
    print("Boleh masuk")
else:
    print("Belum cukup umur")
```

**Dengan early return (di function, nanti Lesson 5)**:

```python
def cek_umur(umur):
    if umur < 18:
        return "Belum cukup umur"
    
    return "Boleh masuk"

print(cek_umur(15))  # Belum cukup umur
```

---

## Contoh Praktis

**Use case 1: Diskon**

```python
total_belanja = 250000

if total_belanja >= 200000:
    diskon = total_belanja * 0.1
    total_akhir = total_belanja - diskon
    print(f"Dapat diskon 10%!")
    print(f"Total bayar: Rp {int(total_akhir):,}")
else:
    print(f"Total bayar: Rp {total_belanja:,}")
    print("(Belanja min 200k dapat diskon 10%)")
```

Output:
```
Dapat diskon 10%!
Total bayar: Rp 225,000
```

**Use case 2: Grading Simple**

```python
nilai = 75

if nilai >= 70:
    print("Lulus")
else:
    print("Tidak lulus, remedial")
```

**Use case 3: Validasi Input**

```python
username = "ab"

if len(username) >= 5:
    print("Username valid")
    # Lanjut proses registrasi
else:
    print("Username minimal 5 karakter")
```

---

## Nested If-Else

If-else di dalam if-else:

```python
umur = 25
punya_sim = False

if umur >= 17:
    if punya_sim:
        print("Boleh nyetir")
    else:
        print("Umur cukup, tapi belum ada SIM")
else:
    print("Umur belum cukup")
```

Output: `Umur cukup, tapi belum ada SIM`

---

## Ternary Operator (Shortcut)

Kalau cuma 1 baris, bisa pake ternary:

**Cara biasa**:

```python
umur = 20

if umur >= 18:
    status = "Dewasa"
else:
    status = "Anak-anak"

print(status)
```

**Shortcut (ternary)**:

```python
umur = 20
status = "Dewasa" if umur >= 18 else "Anak-anak"
print(status)
```

Output sama: `Dewasa`

**Syntax**: `value_if_true if kondisi else value_if_false`

**Kapan pake?** Kalau cuma assign variable. Kalau ada logic banyak, jangan pake (bikin susah dibaca).

---

## Kesalahan Umum

**1. Else tanpa If**

```python
else:  # ❌ SyntaxError
    print("Test")
```

`else` harus ada `if` di atasnya.

**2. Indent salah**

```python
if umur >= 18:
    print("Dewasa")
  else:  # ❌ IndentationError (else ga boleh indent)
```

**Fix**: `else` harus sejajar dengan `if`

```python
if umur >= 18:
    print("Dewasa")
else:  # ✅
    print("Anak-anak")
```

---

Next: **If-Elif-Else** - handle banyak kondisi.
