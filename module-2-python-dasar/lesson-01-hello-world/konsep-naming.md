## Naming & Best Practices

Nama variable itu **penting banget**. Code yang bagus = code yang gampang dibaca orang lain (atau diri lu sendiri 3 bulan kemudian).

---

### Aturan Naming di Python

**Yang BOLEH**:
- Huruf (a-z, A-Z)
- Angka (0-9), **tapi ga boleh di awal**
- Underscore `_`

**Yang GA BOLEH**:
- Spasi
- Karakter khusus (`@`, `#`, `$`, `%`, dll)
- Mulai dengan angka
- Keyword Python (`if`, `for`, `while`, `def`, dll)

**Contoh**:

```python
# ✅ Valid
nama = "Rafi"
umur_sekarang = 25
total_2024 = 1000000
_temp = 123

# ❌ Invalid
nama saya = "Rafi"  # Ada spasi
2024_total = 100    # Mulai dari angka
total$ = 500        # Ada karakter khusus
for = 10            # 'for' adalah keyword Python
```

---

### Convention: snake_case

Python pake **snake_case** buat nama variable: semua huruf kecil, kata dipisah `_`.

```python
# ✅ Good (snake_case)
nama_lengkap = "Rafi Maulana"
harga_total = 50000
jumlah_item_terjual = 15

# ❌ Avoid (camelCase - ini untuk JavaScript)
namaLengkap = "Rafi"
hargaTotal = 50000

# ❌ Avoid (PascalCase - ini untuk class name)
NamaLengkap = "Rafi"
```

> **Note**: `camelCase` dan `PascalCase` ga salah secara syntax. Code lu tetep jalan. Cuma **convention** Python pake `snake_case` biar konsisten.

---

### Descriptive Names

Nama variable harus **jelas** maksudnya apa.

**Bad** (singkatan ambiguous):

```python
n = "Rafi"
t = 50000
x = 123
```

Lu sendiri bingung 2 minggu kemudian: `t` itu apa? Total? Tempo? Tax?

**Good** (jelas):

```python
nama_customer = "Rafi"
total_harga = 50000
jumlah_transaksi = 123
```

Langsung keliatan maksudnya.

---

### Kapan Singkatan Boleh?

Singkatan **boleh** kalau udah jadi standar universal:

```python
# ✅ Acceptable
id_user = 12345
url_website = "https://example.com"
html_content = "<div>Hello</div>"
max_value = 100
min_value = 10
```

Singkatan kayak `id`, `url`, `html`, `max`, `min` udah dipahami semua orang.

**Avoid** singkatan yang lu bikin sendiri:

```python
# ❌ Avoid
jml_trx = 10      # "jumlah_transaksi" lebih jelas
hrgttl = 50000    # "harga_total" lebih jelas
```

---

### Variable Temporary

Buat variable sementara yang umur pendek (loop, debugging), nama pendek **boleh**:

```python
# Loop counter
for i in range(10):
    print(i)

# Temporary value
temp = nilai_a
nilai_a = nilai_b
nilai_b = temp
```

Variable `i` dan `temp` udah jadi convention universal buat temporary value.

---

### Constants (Nilai Tetap)

Kalau nilai ga akan berubah, pake **UPPERCASE**:

```python
# Constants (nilai tetap)
MAX_USERS = 100
TAX_RATE = 0.11
PI = 3.14159
```

Ini bukan aturan wajib Python (Python ga punya true constant). Ini cuma **signal** buat programmer lain: "Jangan ubah value ini!"

---

### Contoh: Bad vs Good

**Bad** (susah dibaca):

```python
x = 15000
y = 5000
z = x * y
print(z)
```

Lu harus baca seluruh code buat ngerti `x` dan `y` itu apa.

**Good** (self-documenting):

```python
harga_per_unit = 15000
jumlah_terjual = 5000
total_pendapatan = harga_per_unit * jumlah_terjual
print(total_pendapatan)
```

Tanpa comment pun udah jelas ini ngitung apa.

---

### Don't Overthink

Jangan terlalu perfeksionis. Nama variable ga harus "perfect" di attempt pertama. **Refactor** itu normal.

**Workflow normal**:
1. Tulis code dulu, pake nama asal-asalan (`x`, `temp`, `data`)
2. Code udah jalan
3. Refactor: ganti nama variable biar lebih jelas
4. Done

VS Code ada fitur "Rename Symbol" (F2) - ganti semua occurrence nama variable sekaligus.

---

## Rangkuman

- **Aturan**: huruf, angka (bukan di awal), underscore
- **Convention**: `snake_case` (huruf kecil, `_` pemisah)
- **Descriptive**: nama jelas maksudnya
- **Singkatan**: boleh kalau standar (`id`, `url`, `max`)
- **Constants**: `UPPERCASE`
- **Temporary**: nama pendek (`i`, `temp`) boleh

Next: **Exercises** - praktek bikin variable sendiri.
