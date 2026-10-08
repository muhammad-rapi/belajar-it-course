## Summary - Conditionals

Selamat! Lu udah bisa bikin program yang "mikir" berdasarkan kondisi.

---

## Yang Udah Lu Pelajari

### 1. If Statement
- Syntax: `if kondisi:`
- Code jalan kalau kondisi `True`
- Indent wajib (4 spasi)

### 2. If-Else
- Dua pilihan: `if` atau `else`
- Salah satu pasti jalan

### 3. If-Elif-Else
- Banyak pilihan (3+)
- Cuma 1 blok yang jalan (yang pertama `True`)
- Urutan penting (dari besar ke kecil kalau pake `>=`)

### 4. Comparison Operators
- `==` `!=` `>` `<` `>=` `<=`
- Return `True` atau `False`

### 5. Logic Operators
- `and` - semua harus True
- `or` - salah satu True
- `not` - balik nilai
- `in` - check membership

---

## Skill yang Lu Kuasai Sekarang

✅ Bikin keputusan berdasarkan kondisi  
✅ Compare nilai dengan operator  
✅ Combine multiple kondisi (and/or)  
✅ Handle banyak pilihan (elif)  
✅ Validasi input user  
✅ Debugging conditional logic  

---

## Pattern yang Sering Dipake

**1. Range check**

```python
if 18 <= umur <= 60:
    print("Dewasa")
```

**2. Multiple validation**

```python
if len(username) >= 5 and "@" in email and umur >= 13:
    print("Registrasi valid")
```

**3. Early return (di function nanti)**

```python
if kondisi_error:
    return "Error"

# Lanjut proses normal
```

**4. Default value**

```python
diskon = 0
if is_member:
    diskon = 10
elif total >= 500000:
    diskon = 20
```

---

## Next Steps

**Next lesson: Loops (For & While)** - ngulang code otomatis.

Preview:

```python
# Print 1-10 tanpa nulis 10 baris
for i in range(1, 11):
    print(i)

# Loop list
buah = ["apel", "jeruk", "mangga"]
for item in buah:
    print(item)

# While loop
saldo = 100000
while saldo > 0:
    saldo -= 10000
    print(f"Sisa: {saldo}")
```

Sebelum lanjut, **pastiin lu udah**:
- [ ] Ngerjain semua 5 exercises
- [ ] Paham perbedaan `and` vs `or`
- [ ] Paham kapan pake `if`, `if-else`, atau `if-elif-else`
- [ ] Bisa debug conditional logic (print variable)

---

## Tips Debugging Conditionals

**1. Print kondisi**

```python
print(f"umur >= 18: {umur >= 18}")
print(f"punya_sim: {punya_sim}")

if umur >= 18 and punya_sim:
    print("Boleh nyetir")
```

**2. Check satu-satu**

```python
# Kalau bingung kenapa ga jalan, pecah:
if umur >= 18:
    print("Umur cukup")
    if punya_sim:
        print("Punya SIM")
```

**3. Test boundary values**

Kalau kondisi `nilai >= 80`, test dengan:
- `79` (harusnya False)
- `80` (harusnya True)
- `81` (harusnya True)

---

## Challenge (Optional)

**Mini Project: Simple Quiz App**

Bikin quiz 5 soal dengan scoring:

```python
score = 0

# Soal 1
jawaban1 = "B"
if jawaban1 == "B":
    score += 10
    print("Soal 1: Benar (+10)")
else:
    print("Soal 1: Salah")

# ... soal 2-5 ...

# Grading
if score >= 80:
    print(f"Score: {score} - Grade A")
elif score >= 60:
    print(f"Score: {score} - Grade B")
else:
    print(f"Score: {score} - Grade C")
```

<details>
<summary><strong>Full Solution</strong></summary>

```python
print("=== Quiz Python Dasar ===\n")
score = 0

# Soal 1
print("1. Python adalah bahasa pemrograman?")
print("A. Compiled")
print("B. Interpreted")
jawaban1 = "B"
if jawaban1 == "B":
    score += 10
    print("✓ Benar (+10)\n")
else:
    print("✗ Salah\n")

# Soal 2
print("2. Syntax if yang benar:")
print("A. if x = 5:")
print("B. if x == 5:")
jawaban2 = "B"
if jawaban2 == "B":
    score += 10
    print("✓ Benar (+10)\n")
else:
    print("✗ Salah\n")

# Soal 3
print("3. Operator logika untuk 'semua harus True':")
print("A. and")
print("B. or")
jawaban3 = "A"
if jawaban3 == "A":
    score += 10
    print("✓ Benar (+10)\n")
else:
    print("✗ Salah\n")

# Soal 4
print("4. Range 18 <= umur <= 60 artinya:")
print("A. umur >= 18 and umur <= 60")
print("B. umur >= 18 or umur <= 60")
jawaban4 = "A"
if jawaban4 == "A":
    score += 10
    print("✓ Benar (+10)\n")
else:
    print("✗ Salah\n")

# Soal 5
print("5. Indent di Python:")
print("A. Optional")
print("B. Wajib")
jawaban5 = "B"
if jawaban5 == "B":
    score += 10
    print("✓ Benar (+10)\n")
else:
    print("✗ Salah\n")

# Grading
print("=" * 30)
if score == 50:
    print(f"Score: {score}/50 - Perfect! Grade A+")
elif score >= 40:
    print(f"Score: {score}/50 - Excellent! Grade A")
elif score >= 30:
    print(f"Score: {score}/50 - Good! Grade B")
elif score >= 20:
    print(f"Score: {score}/50 - OK. Grade C")
else:
    print(f"Score: {score}/50 - Perlu belajar lagi. Grade D")
```
</details>

---

Ready buat Lesson 4? Let's loop! 🔁
