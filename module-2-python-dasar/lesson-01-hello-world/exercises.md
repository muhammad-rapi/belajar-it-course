## Exercises - Hello World & Variables

Waktunya praktek. **Ketik ulang semua code**, jangan copy-paste. Lu perlu muscle memory.

---

### Exercise 1: Personal Info Card

**Tujuan**: Bikin program yang nampilin info diri lu.

**Yang Perlu Lu Lakukan**:
1. Bikin file `personal_info.py`
2. Bikin 5 variable:
   - `nama_lengkap` (string)
   - `umur` (integer)
   - `kota` (string)
   - `hobi` (string)
   - `status` (string, misal: "Pelajar" atau "Kerja")
3. Print semua variable

**Expected Output** (contoh):
```
Rafi Maulana
25
Jakarta
Main game
Kerja
```

<details>
<summary><strong>Hint 1</strong></summary>

Syntax bikin variable: `nama_variable = value`

String harus pake kutip: `nama = "Rafi"`
</details>

<details>
<summary><strong>Hint 2</strong></summary>

Print satu variable per baris:
```python
print(nama_lengkap)
print(umur)
# dst...
```
</details>

<details>
<summary><strong>Solusi</strong></summary>

```python
nama_lengkap = "Rafi Maulana"
umur = 25
kota = "Jakarta"
hobi = "Main game"
status = "Kerja"

print(nama_lengkap)
print(umur)
print(kota)
print(hobi)
print(status)
```

**Bonus** (pake f-string biar lebih rapi):
```python
nama_lengkap = "Rafi Maulana"
umur = 25
kota = "Jakarta"
hobi = "Main game"
status = "Kerja"

print(f"Nama: {nama_lengkap}")
print(f"Umur: {umur} tahun")
print(f"Kota: {kota}")
print(f"Hobi: {hobi}")
print(f"Status: {status}")
```
</details>

---

### Exercise 2: Kalkulator Warung

**Tujuan**: Hitung total belanja warung.

**Yang Perlu Lu Lakukan**:
1. Bikin file `warung.py`
2. Bikin variable harga untuk 3 item:
   - `harga_nasi_goreng` = 15000
   - `harga_teh` = 3000
   - `harga_gorengan` = 1000
3. Hitung `total` (jumlah semua harga)
4. Print total

**Expected Output**:
```
19000
```

<details>
<summary><strong>Hint</strong></summary>

Pake operator `+` buat tambah angka:
```python
total = harga1 + harga2 + harga3
```
</details>

<details>
<summary><strong>Solusi</strong></summary>

```python
harga_nasi_goreng = 15000
harga_teh = 3000
harga_gorengan = 1000

total = harga_nasi_goreng + harga_teh + harga_gorengan
print(total)
```

**Bonus** (format rupiah):
```python
harga_nasi_goreng = 15000
harga_teh = 3000
harga_gorengan = 1000

total = harga_nasi_goreng + harga_teh + harga_gorengan
print(f"Total: Rp {total:,}")  # Output: Total: Rp 19,000
```
</details>

---

### Exercise 3: Update Saldo

**Tujuan**: Simulasi transaksi - saldo berkurang/bertambah.

**Yang Perlu Lu Lakukan**:
1. Bikin file `saldo.py`
2. Bikin variable `saldo` = 100000
3. Print saldo awal
4. Kurangi 25000 (belanja)
5. Print saldo setelah belanja
6. Tambah 50000 (dapat transfer)
7. Print saldo akhir

**Expected Output**:
```
100000
75000
125000
```

<details>
<summary><strong>Hint</strong></summary>

Update variable pake `=`:
```python
saldo = saldo - 25000
# atau shortcut:
saldo -= 25000
```
</details>

<details>
<summary><strong>Solusi</strong></summary>

```python
saldo = 100000
print(saldo)

saldo = saldo - 25000
print(saldo)

saldo = saldo + 50000
print(saldo)
```

**Atau pake shortcut**:
```python
saldo = 100000
print(saldo)

saldo -= 25000
print(saldo)

saldo += 50000
print(saldo)
```
</details>

---

### Exercise 4: Ganti Nama Variable yang Jelek

**Tujuan**: Refactor code - ganti nama variable yang ambiguous.

**Code awal** (save jadi `refactor.py`):
```python
x = "Budi"
y = 30
z = 175.5

print(x)
print(y)
print(z)
```

**Yang Perlu Lu Lakukan**:
Ganti `x`, `y`, `z` jadi nama yang descriptive. Misal: `nama`, `umur`, `tinggi`.

<details>
<summary><strong>Solusi</strong></summary>

```python
nama = "Budi"
umur = 30
tinggi_cm = 175.5

print(nama)
print(umur)
print(tinggi_cm)
```

Atau lebih rapi lagi:
```python
nama = "Budi"
umur = 30
tinggi_cm = 175.5

print(f"Nama: {nama}")
print(f"Umur: {umur} tahun")
print(f"Tinggi: {tinggi_cm} cm")
```
</details>

---

### Exercise 5: Challenge - Hitung Diskon

**Tujuan**: Hitung harga setelah diskon.

**Yang Perlu Lu Lakukan**:
1. Bikin file `diskon.py`
2. Bikin variable:
   - `harga_asli` = 200000
   - `persentase_diskon` = 20 (artinya 20%)
3. Hitung `jumlah_diskon` (20% dari harga asli)
4. Hitung `harga_akhir` (harga asli - diskon)
5. Print `harga_asli`, `jumlah_diskon`, dan `harga_akhir`

**Expected Output**:
```
200000
40000
160000
```

<details>
<summary><strong>Hint 1</strong></summary>

20% = 20/100 = 0.2

Jadi: `jumlah_diskon = harga_asli * 0.2`
</details>

<details>
<summary><strong>Hint 2</strong></summary>

Atau langsung: `jumlah_diskon = harga_asli * (persentase_diskon / 100)`
</details>

<details>
<summary><strong>Solusi</strong></summary>

```python
harga_asli = 200000
persentase_diskon = 20

jumlah_diskon = harga_asli * (persentase_diskon / 100)
harga_akhir = harga_asli - jumlah_diskon

print(harga_asli)
print(int(jumlah_diskon))  # int() biar ga ada desimal
print(int(harga_akhir))
```

**Atau pake format rapi**:
```python
harga_asli = 200000
persentase_diskon = 20

jumlah_diskon = harga_asli * (persentase_diskon / 100)
harga_akhir = harga_asli - jumlah_diskon

print(f"Harga asli: Rp {harga_asli:,}")
print(f"Diskon ({persentase_diskon}%): Rp {int(jumlah_diskon):,}")
print(f"Harga akhir: Rp {int(harga_akhir):,}")
```

Output:
```
Harga asli: Rp 200,000
Diskon (20%): Rp 40,000
Harga akhir: Rp 160,000
```
</details>

---

## Checklist

Abis ngerjain semua exercise, cek:
- [ ] Semua file jalan tanpa error
- [ ] Output sesuai expected
- [ ] Nama variable descriptive (bukan `x`, `y`, `z`)
- [ ] Lu ngetik ulang, bukan copy-paste

**Stuck?** Baca error message-nya. Python kasih tau line mana yang error. Baca pelan-pelan, error message Python lumayan helpful.

Next: **Kesalahan Umum** - bug yang sering bikin frustasi (dan cara fixnya).
