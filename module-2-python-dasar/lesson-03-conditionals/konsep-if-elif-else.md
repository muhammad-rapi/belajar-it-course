## If-Elif-Else - Banyak Pilihan

`if-else` cuma bisa 2 pilihan. Kalau lu butuh **3+ pilihan**, pake **elif** (else if).

---

### Syntax

```python
if kondisi1:
    # Jalan kalau kondisi1 True
elif kondisi2:
    # Jalan kalau kondisi1 False, kondisi2 True
elif kondisi3:
    # Jalan kalau kondisi1 & kondisi2 False, kondisi3 True
else:
    # Jalan kalau semua kondisi False
```

**Aturan**:
- `elif` cuma cek kalau kondisi sebelumnya `False`
- Begitu ada 1 kondisi `True`, sisanya di-skip
- `else` optional (boleh ada, boleh ga)

---

### Contoh 1: Grading

```python
nilai = 85

if nilai >= 90:
    print("Grade: A")
elif nilai >= 80:
    print("Grade: B")
elif nilai >= 70:
    print("Grade: C")
elif nilai >= 60:
    print("Grade: D")
else:
    print("Grade: E (Tidak Lulus)")
```

Output: `Grade: B`

**Kenapa B?** 
- `85 >= 90`? False, skip
- `85 >= 80`? **True, jalan ini, sisanya di-skip**

---

### Contoh 2: Harga Tiket Bioskop

```python
umur = 15

if umur < 5:
    harga = 0
    print("Gratis (balita)")
elif umur < 12:
    harga = 30000
    print(f"Harga anak: Rp {harga:,}")
elif umur < 60:
    harga = 50000
    print(f"Harga normal: Rp {harga:,}")
else:
    harga = 35000
    print(f"Harga senior: Rp {harga:,}")
```

Output: `Harga normal: Rp 50,000`

(Umur 15 → masuk kategori 12-59)

---

### Contoh 3: Traffic Light

```python
lampu = "kuning"

if lampu == "hijau":
    print("Jalan")
elif lampu == "kuning":
    print("Hati-hati, siap berhenti")
elif lampu == "merah":
    print("Berhenti")
else:
    print("Lampu error")
```

Output: `Hati-hati, siap berhenti`

---

### Elif vs Multiple If

**Multiple If** (SEMUA dicek):

```python
nilai = 85

if nilai >= 90:
    print("A")
if nilai >= 80:
    print("B")  # Jalan
if nilai >= 70:
    print("C")  # Jalan juga!
```

Output:
```
B
C
```

Semua kondisi yang `True` jalan (ga bagus buat grading).

**Elif** (cuma 1 yang jalan):

```python
nilai = 85

if nilai >= 90:
    print("A")
elif nilai >= 80:
    print("B")  # Jalan, sisanya di-skip
elif nilai >= 70:
    print("C")  # Ga dicek
```

Output:
```
B
```

Cuma yang pertama `True` yang jalan.

**Rule**: Kalau lu cuma mau **1 kondisi jalan**, pake `elif`. Kalau mau **semua kondisi dicek**, pake multiple `if`.

---

### Contoh 4: BMI Category

```python
berat = 70  # kg
tinggi = 1.75  # meter
bmi = berat / (tinggi ** 2)

print(f"BMI: {bmi:.1f}")

if bmi < 18.5:
    print("Underweight")
elif bmi < 25:
    print("Normal")
elif bmi < 30:
    print("Overweight")
else:
    print("Obesitas")
```

Output:
```
BMI: 22.9
Normal
```

---

### Order Matters (Urutan Penting)

**❌ Salah (urutan kebalik)**:

```python
nilai = 85

if nilai >= 70:
    print("C")  # Jalan di sini, sisanya di-skip
elif nilai >= 80:
    print("B")  # Ga pernah dicek
elif nilai >= 90:
    print("A")  # Ga pernah dicek
```

Output: `C` (padahal harusnya B)

**✅ Benar (dari besar ke kecil)**:

```python
nilai = 85

if nilai >= 90:
    print("A")
elif nilai >= 80:
    print("B")  # Jalan di sini
elif nilai >= 70:
    print("C")
```

Output: `B` (benar)

**Rule**: Kalau pake `>=`, mulai dari **nilai terbesar** ke terkecil.

---

### Nested Elif

Elif di dalam if:

```python
umur = 25
punya_sim = True
punya_mobil = False

if umur >= 17:
    if punya_sim:
        if punya_mobil:
            print("Boleh nyetir sendiri")
        else:
            print("Boleh nyetir, tapi sewa/pinjem mobil")
    else:
        print("Umur cukup, tapi belum ada SIM")
else:
    print("Umur belum cukup")
```

**Note**: Kalau banyak nested, code jadi susah dibaca. Nanti di Lesson 5 (Functions) kita refactor jadi lebih rapi.

---

## Contoh Praktis

**Use case 1: Kalkulator Pajak**

```python
penghasilan = 60000000  # per tahun

if penghasilan <= 50000000:
    pajak = 0
elif penghasilan <= 100000000:
    pajak = penghasilan * 0.05
elif penghasilan <= 250000000:
    pajak = penghasilan * 0.15
else:
    pajak = penghasilan * 0.25

print(f"Penghasilan: Rp {penghasilan:,}")
print(f"Pajak: Rp {int(pajak):,}")
```

**Use case 2: Quiz App**

```python
jawaban = "B"

if jawaban == "A":
    print("Salah")
elif jawaban == "B":
    print("Benar! +10 poin")
elif jawaban == "C":
    print("Salah")
elif jawaban == "D":
    print("Salah")
else:
    print("Jawaban tidak valid")
```

---

## Rangkuman

| Struktur | Kapan Pake |
|----------|-----------|
| `if` | 1 kondisi, ga ada alternatif |
| `if-else` | 2 pilihan (A atau B) |
| `if-elif-else` | 3+ pilihan (A, B, C, atau D) |
| Multiple `if` | Semua kondisi harus dicek |

---

Next: **Comparison & Logic Operators** - combine multiple kondisi.
