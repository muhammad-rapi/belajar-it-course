## Kesalahan Umum - Hello World & Variables

Bug-bug yang paling sering bikin frustasi pemula (dan cara fixnya).

---

### 1. NameError: name '...' is not defined

**Error paling sering muncul.**

```python
print(nama)  # SALAH: NameError: name 'nama' is not defined
nama = "Rafi"
```

**Penyebab**:
- Variable dipake sebelum didefinisikan
- Typo nama variable
- Lupa kutip untuk string

**Fix**:
```python
# BENAR: Definisikan dulu, baru pake
nama = "Rafi"
print(nama)

# BENAR: Cek typo
nama = "Rafi"
print(nama)  # bukan "nma" atau "Nama"

# BENAR: String harus pake kutip
print("Rafi")  # bukan print(Rafi)
```

---

### 2. SyntaxError: invalid syntax

**Error umum kedua.**

```python
print "Hello"  # SALAH: SyntaxError (Python 3 wajib pake kurung)
```

**Penyebab**:
- Lupa kurung di `print()`
- Lupa kutip di string
- Typo operator

**Fix**:
```python
# BENAR: Python 3 wajib kurung
print("Hello")

# BENAR: String harus pake kutip
nama = "Rafi"  # bukan nama = Rafi

# BENAR: Assignment pake `=`, bukan `==`
nama = "Rafi"  # bukan nama == "Rafi"
```

---

### 3. TypeError: unsupported operand type(s)

**Terjadi waktu operasi matematika sama tipe data salah.**

```python
umur = "25"  # Ini string, bukan angka
umur_tahun_depan = umur + 1  # SALAH: TypeError
```

**Penyebab**: Operasi matematika sama string.

**Fix**: Pastiin tipe data bener.

```python
# BENAR: Bikin umur jadi integer (angka)
umur = 25  # bukan "25"
umur_tahun_depan = umur + 1
print(umur_tahun_depan)  # 26
```

**Atau convert dulu**:
```python
umur = "25"  # String dari input user
umur_int = int(umur)  # Convert ke integer
umur_tahun_depan = umur_int + 1
print(umur_tahun_depan)  # 26
```

---

### 4. Lupa Save File

**Code ga berubah padahal udah edit.**

**Penyebab**: Lu lupa save file sebelum run.

**Fix**:
- Save dulu: `Ctrl+S` (Windows/Linux) atau `Cmd+S` (Mac)
- Atau enable "Auto Save" di VS Code: File → Auto Save

Dot putih di tab file = belum di-save. Ga ada dot = udah di-save.

---

### 5. Run File yang Salah

**Lu edit `hello.py`, tapi run `test.py`.**

**Penyebab**: Di Terminal, lu run file lain.

**Fix**: Pastiin nama file yang lu run sesuai.

```bash
# Cek file apa yang lu edit
ls

# Run file yang bener
python3 hello.py  # bukan python3 test.py
```

---

### 6. IndentationError (Preview)

**Akan sering muncul nanti waktu belajar function/loop.**

```python
nama = "Rafi"
  print(nama)  # SALAH: IndentationError: unexpected indent
```

**Penyebab**: Ada spasi/tab di awal line yang ga perlu.

**Fix**: Jangan indent kalau ga perlu. Indent cuma buat block code (function, loop, if).

```python
nama = "Rafi"
print(nama)  # BENAR: Ga ada indent
```

---

### 7. Print Variable Tanpa Kutip vs Dengan Kutip

**Newbie sering bingung kapan pake kutip.**

```python
nama = "Rafi"
print("nama")   # Output: nama (literal string)
print(nama)     # Output: Rafi (value variable)
```

**Aturan**:
- **Pake kutip** = print literal text
- **Tanpa kutip** = print value variable

```python
umur = 25
print("umur")   # Output: umur
print(umur)     # Output: 25
print("Umur:", umur)  # Output: Umur: 25
```

---

### 8. Update Variable yang Salah

**Lupa assign ulang variable.**

```python
saldo = 100000
saldo - 50000  # SALAH: Ini ga ngapa-ngapain
print(saldo)   # Output: 100000 (belum berubah)
```

**Penyebab**: Lupa `=` buat assign hasil ke variable.

**Fix**:
```python
saldo = 100000
saldo = saldo - 50000  # BENAR: Assign ulang
print(saldo)   # Output: 50000
```

---

### 9. Case Sensitivity

**Python case-sensitive. `nama` ≠ `Nama` ≠ `NAMA`.**

```python
nama = "Rafi"
print(Nama)  # SALAH: NameError: name 'Nama' is not defined
```

**Fix**: Ketik persis sama.

```python
nama = "Rafi"
print(nama)  # BENAR: ```

---

### 10. Path File Salah (Advanced)

**File ga ketemu waktu run.**

```bash
python3 hello.py
# Error: No such file or directory
```

**Penyebab**: Terminal lu bukan di folder yang bener.

**Fix**: Pindah ke folder yang bener.

```bash
# Cek lu ada dimana
pwd

# Pindah ke folder project
cd ~/belajar-python

# Sekarang run
python3 hello.py
```

---

## Tips Debugging

Waktu stuck:

1. **Baca error message** - Python kasih tau line mana yang error
2. **Cek line yang error** - biasanya masalahnya di situ atau line sebelumnya
3. **Print variable** - pastiin value-nya sesuai ekspektasi
   ```python
   print(f"DEBUG: nama = {nama}")
   ```
4. **Google error message** - copy paste error ke Google, biasanya ada solusi
5. **Restart Terminal** - kadang Terminal nge-cache code lama

**Stuck lebih dari 15 menit?** Break dulu 5 menit. Balik lagi sering langsung ketemu masalahnya.

---

Next: **Summary** - ringkasan lesson ini + next steps.
