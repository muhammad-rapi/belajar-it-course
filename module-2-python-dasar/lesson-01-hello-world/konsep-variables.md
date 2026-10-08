## Variables - Cara Simpen Data

Bayangin lu punya warung. Tiap hari lu catat:
- Jumlah gorengan terjual
- Total uang masuk
- Nama supplier

Lu simpen data itu di **buku catatan**. Besok lu buka lagi, datanya masih ada.

Di programming, **variable = buku catatan komputer**. Lu simpen data, kasih nama, terus bisa dipake kapan aja.

---

### Bikin Variable Pertama

Buka file baru: `variables.py`

```python
nama = "Rafi"
umur = 25
```

Itu doang. Lu udah bikin 2 variable:
- Variable `nama` isinya `"Rafi"`
- Variable `umur` isinya `25`

Sekarang `print`:

```python
nama = "Rafi"
umur = 25

print(nama)
print(umur)
```

Run. Output:
```
Rafi
25
```

---

### Apa yang Terjadi?

```python
nama = "Rafi"
```

- **`nama`** = nama variable (lu yang tentuin, bebas)
- **`=`** = operator assignment (kasih nilai)
- **`"Rafi"`** = value (isinya)

**Bayangin kayak kotak dengan label**:

```
┌─────────────┐
│   nama      │  ← label (nama variable)
├─────────────┤
│   "Rafi"    │  ← isi (value)
└─────────────┘
```

Komputer nyimpen value `"Rafi"` di memory, terus kasih label `nama` biar lu bisa akses lagi.

---

### Kenapa Pake Variable?

**Tanpa variable** (hard-coded):

```python
print("Hello, Rafi!")
print("Rafi, umur kamu 25 tahun")
print("Email: rafi@gmail.com")
```

Kalau mau ganti nama, lu harus edit 3 tempat. Ribet.

**Pake variable**:

```python
nama = "Rafi"
umur = 25
email = "rafi@gmail.com"

print(f"Hello, {nama}!")
print(f"{nama}, umur kamu {umur} tahun")
print(f"Email: {email}")
```

Mau ganti nama? Tinggal edit **satu tempat** (baris pertama). Sisanya otomatis update.

> **f-string** (`f"..."`) = cara masukin variable ke dalam text. Nanti kita bahas lebih dalam di Lesson 2.

---

### Jenis-Jenis Data (Preview)

Python punya beberapa tipe data:

```python
# String (text) - pake kutip
nama = "Budi"
alamat = 'Jakarta'  # kutip satu atau dua sama aja

# Integer (angka bulat)
umur = 30
jumlah_anak = 2

# Float (angka desimal)
tinggi = 175.5
berat = 68.3

# Boolean (benar/salah)
sudah_nikah = True
punya_mobil = False
```

Beda tipe data punya behavior beda. Kita bahas detail di Lesson 2.

---

### Ubah Nilai Variable

Variable itu **bisa diubah** (makanya namanya variable, bukan constant):

```python
saldo = 100000
print(saldo)  # Output: 100000

saldo = 50000  # Ganti isinya
print(saldo)  # Output: 50000
```

Value lama (100000) **ditimpa** sama value baru (50000). Ga ada yang bilang error.

---

### Operasi Matematika

Lu bisa operasi langsung sama variable:

```python
harga_nasi = 15000
harga_teh = 5000

total = harga_nasi + harga_teh
print(total)  # Output: 20000
```

Operasi dasar:
- `+` = tambah
- `-` = kurang
- `*` = kali
- `/` = bagi
- `**` = pangkat (misal: `2 ** 3` = 8)
- `%` = modulo (sisa bagi, misal: `10 % 3` = 1)

---

### Update Variable

Lu bisa update variable pake nilai lama-nya:

```python
saldo = 100000
print(saldo)  # 100000

saldo = saldo + 50000  # Tambah 50k
print(saldo)  # 150000
```

Shortcut (sama aja):

```python
saldo = 100000
saldo += 50000  # Sama dengan: saldo = saldo + 50000
print(saldo)  # 150000
```

Shortcut lain:
- `saldo -= 20000` → kurangi 20k
- `saldo *= 2` → kali 2
- `saldo /= 2` → bagi 2

---

### Kesalahan Umum

#### 1. Pake Variable Sebelum Didefinisikan

```python
print(nama)  # ❌ NameError: name 'nama' is not defined
nama = "Rafi"
```

**Fix**: Definisikan dulu, baru pake.

```python
nama = "Rafi"  # ✅ Definisikan dulu
print(nama)
```

#### 2. Typo Nama Variable

```python
nama = "Rafi"
print(nma)  # ❌ NameError: name 'nma' is not defined
```

Python **case-sensitive**: `nama` ≠ `Nama` ≠ `NAMA`.

**Fix**: Ketik persis sama kayak waktu definisikan.

#### 3. Lupa Kutip untuk String

```python
nama = Rafi  # ❌ NameError: name 'Rafi' is not defined
```

**Fix**: Text harus pake kutip.

```python
nama = "Rafi"  # ✅
```

---

## Rangkuman

- **Variable** = tempat simpen data di memory
- Syntax: `nama_variable = value`
- Bisa diubah kapan aja
- Python case-sensitive
- Tipe data: string, int, float, boolean (detail di Lesson 2)

Next: **Naming & Best Practices** - aturan naming yang bener biar code lu ga berantakan.
