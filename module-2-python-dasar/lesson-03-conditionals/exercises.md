## Exercises - Conditionals

Waktunya praktek if-elif-else!

---

### Exercise 1: Kalkulator Diskon

**Tujuan**: Hitung diskon berdasarkan total belanja.

**Rules**:
- Belanja < 100k → ga ada diskon
- Belanja 100k-500k → diskon 10%
- Belanja > 500k → diskon 20%

**Yang Perlu Lu Lakukan**:
1. Bikin file `diskon.py`
2. Bikin variable `total_belanja` (misal: 350000)
3. Hitung diskon dan total akhir
4. Print hasilnya

**Expected Output** (total = 350000):
```
Total belanja: Rp 350,000
Diskon: 10% (Rp 35,000)
Total bayar: Rp 315,000
```

<details>
<summary><strong>Hint</strong></summary>

```python
if total_belanja < 100000:
    diskon_persen = 0
elif total_belanja <= 500000:
    diskon_persen = 10
else:
    diskon_persen = 20
```
</details>

<details>
<summary><strong>Solusi</strong></summary>

```python
total_belanja = 350000

if total_belanja < 100000:
    diskon_persen = 0
elif total_belanja <= 500000:
    diskon_persen = 10
else:
    diskon_persen = 20

diskon_rupiah = total_belanja * (diskon_persen / 100)
total_bayar = total_belanja - diskon_rupiah

print(f"Total belanja: Rp {total_belanja:,}")
print(f"Diskon: {diskon_persen}% (Rp {int(diskon_rupiah):,})")
print(f"Total bayar: Rp {int(total_bayar):,}")
```
</details>

---

### Exercise 2: Kalkulator Grade

**Tujuan**: Convert nilai angka jadi grade huruf.

**Rules**:
- 90-100 → A
- 80-89 → B
- 70-79 → C
- 60-69 → D
- < 60 → E (Tidak Lulus)

**Yang Perlu Lu Lakukan**:
1. Bikin file `grade.py`
2. Bikin variable `nilai` (misal: 85)
3. Tentukan grade
4. Print hasil

**Expected Output** (nilai = 85):
```
Nilai: 85
Grade: B
Status: Lulus
```

<details>
<summary><strong>Solusi</strong></summary>

```python
nilai = 85

if nilai >= 90:
    grade = "A"
elif nilai >= 80:
    grade = "B"
elif nilai >= 70:
    grade = "C"
elif nilai >= 60:
    grade = "D"
else:
    grade = "E"

status = "Lulus" if nilai >= 60 else "Tidak Lulus"

print(f"Nilai: {nilai}")
print(f"Grade: {grade}")
print(f"Status: {status}")
```
</details>

---

### Exercise 3: Login Simple

**Tujuan**: Simulasi login dengan username & password.

**Yang Perlu Lu Lakukan**:
1. Bikin file `login.py`
2. Set username dan password yang benar (misal: "admin" dan "12345")
3. Bikin variable input user (misal: "admin" dan "salah")
4. Check apakah keduanya cocok
5. Print "Login berhasil" atau "Username/password salah"

**Expected Output** (username benar, password salah):
```
Login gagal
Username/password salah
```

<details>
<summary><strong>Hint</strong></summary>

Pake `and`: `if username == ... and password == ...`
</details>

<details>
<summary><strong>Solusi</strong></summary>

```python
# Data yang benar
username_benar = "admin"
password_benar = "12345"

# Input user
input_username = "admin"
input_password = "salah"

if input_username == username_benar and input_password == password_benar:
    print("Login berhasil!")
    print(f"Selamat datang, {input_username}")
else:
    print("Login gagal")
    print("Username/password salah")
```

**Bonus** (detailed error):

```python
username_benar = "admin"
password_benar = "12345"

input_username = "admin"
input_password = "salah"

if input_username != username_benar:
    print("Username salah")
elif input_password != password_benar:
    print("Password salah")
else:
    print("Login berhasil!")
```
</details>

---

### Exercise 4: Kalkulator BMI

**Tujuan**: Hitung BMI dan kategori.

**Formula**: `BMI = berat / (tinggi ** 2)`

**Kategori**:
- < 18.5 → Underweight
- 18.5-24.9 → Normal
- 25-29.9 → Overweight
- >= 30 → Obesitas

**Yang Perlu Lu Lakukan**:
1. Bikin file `bmi.py`
2. Set `berat` (kg) dan `tinggi` (meter)
3. Hitung BMI
4. Tentukan kategori
5. Print hasil

**Expected Output** (berat=70, tinggi=1.75):
```
Berat: 70 kg
Tinggi: 1.75 m
BMI: 22.9
Kategori: Normal
```

<details>
<summary><strong>Solusi</strong></summary>

```python
berat = 70  # kg
tinggi = 1.75  # meter

bmi = berat / (tinggi ** 2)

if bmi < 18.5:
    kategori = "Underweight"
elif bmi < 25:
    kategori = "Normal"
elif bmi < 30:
    kategori = "Overweight"
else:
    kategori = "Obesitas"

print(f"Berat: {berat} kg")
print(f"Tinggi: {tinggi} m")
print(f"BMI: {bmi:.1f}")
print(f"Kategori: {kategori}")
```
</details>

---

### Exercise 5: Challenge - Validasi Password

**Tujuan**: Check apakah password memenuhi kriteria keamanan.

**Kriteria**:
- Min 8 karakter
- Harus ada angka
- Harus ada huruf besar

**Yang Perlu Lu Lakukan**:
1. Bikin file `password_validator.py`
2. Set variable `password` (misal: "Abc12345")
3. Check 3 kriteria
4. Print "Password valid" atau list error

**Expected Output** (password="abc123"):
```
Password tidak valid:
- Min 8 karakter
- Harus ada huruf besar
```

<details>
<summary><strong>Hint 1</strong></summary>

```python
len(password) >= 8  # Check panjang
password.isupper()  # Check ada huruf besar
password.isdigit()  # Check ada angka
```
</details>

<details>
<summary><strong>Hint 2</strong></summary>

Pake `any()`:

```python
has_digit = any(char.isdigit() for char in password)
has_upper = any(char.isupper() for char in password)
```
</details>

<details>
<summary><strong>Solusi</strong></summary>

```python
password = "abc123"

# Check criteria
panjang_cukup = len(password) >= 8
ada_angka = any(char.isdigit() for char in password)
ada_huruf_besar = any(char.isupper() for char in password)

# Validasi
if panjang_cukup and ada_angka and ada_huruf_besar:
    print("Password valid ✓")
else:
    print("Password tidak valid:")
    if not panjang_cukup:
        print("- Min 8 karakter")
    if not ada_angka:
        print("- Harus ada angka")
    if not ada_huruf_besar:
        print("- Harus ada huruf besar")
```

**Test cases**:

```python
# Test 1: "abc123" → Error: panjang + huruf besar
# Test 2: "Abc12345" → Valid
# Test 3: "Password" → Error: angka
# Test 4: "12345678" → Error: huruf besar
```
</details>

---

## Checklist

Abis ngerjain:
- [ ] Semua file jalan tanpa error
- [ ] Output sesuai expected
- [ ] Paham kenapa kondisi True/False
- [ ] Coba ubah nilai, cek output berubah

**Stuck?** Print variable buat debug:

```python
print(f"DEBUG: nilai = {nilai}, grade = {grade}")
```

---

Next: **Summary** - ringkasan lesson + next steps.
