## Summary - Hello World & Variables

Selamat! Lu udah nulis program Python pertama dan paham cara komputer simpen data.

---

## Yang Udah Lu Pelajari

### 1. Hello World
- `print()` = fungsi buat nampilin output
- String (text) harus pake kutip `"..."` atau `'...'`
- Python case-sensitive: `print` ≠ `Print`

### 2. Variables
- Variable = tempat simpen data di memory
- Syntax: `nama_variable = value`
- Bisa diubah kapan aja (makanya namanya *variable*)
- Tipe data: string, int, float, boolean

### 3. Operasi Matematika
- `+` tambah, `-` kurang, `*` kali, `/` bagi
- `**` pangkat, `%` modulo (sisa bagi)
- Shortcut: `+=`, `-=`, `*=`, `/=`

### 4. Naming Convention
- `snake_case` (huruf kecil, `_` pemisah)
- Nama descriptive (bukan `x`, `y`, `z`)
- Constants pake `UPPERCASE`

### 5. Common Errors
- `NameError` → variable belum didefinisikan atau typo
- `SyntaxError` → syntax salah (lupa kurung, kutip, dll)
- `TypeError` → operasi sama tipe data yang salah

---

## Skill yang Lu Kuasai Sekarang

✅ Nulis dan run program Python  
✅ Bikin dan update variable  
✅ Print output ke Terminal  
✅ Operasi matematika dasar  
✅ Naming yang bener  
✅ Debugging error sederhana  

---

## Next Steps

Sekarang lu udah bisa bikin program sederhana. **Next lesson**: Data Types & Operations.

Di Lesson 2, lu bakal belajar:
- **String manipulation** - potong, gabung, format text
- **List** - simpen banyak data sekaligus
- **Dictionary** - simpen data pake key-value
- **Type conversion** - ubah string jadi int, int jadi string

Preview singkat:

```python
# String manipulation
nama = "rafi maulana"
print(nama.upper())  # Output: RAFI MAULANA

# List (array)
buah = ["apel", "jeruk", "mangga"]
print(buah[0])  # Output: apel

# Dictionary (object)
user = {
    "nama": "Rafi",
    "umur": 25
}
print(user["nama"])  # Output: Rafi
```

Sebelum lanjut ke Lesson 2, **pastiin lu udah**:
- [ ] Ngerjain semua 5 exercises
- [ ] Code lu jalan tanpa error
- [ ] Paham kenapa variable penting
- [ ] Bisa naming variable yang descriptive

---

## Challenge (Optional)

Sebelum lanjut, coba bikin program ini **tanpa liat solution**:

**Mini Project: Kalkulator BMI (Body Mass Index)**

Input:
- `nama` (string)
- `berat` (kg, float)
- `tinggi` (meter, float)

Hitung BMI: `bmi = berat / (tinggi ** 2)`

Output:
```
Nama: Rafi
Berat: 70 kg
Tinggi: 1.75 m
BMI: 22.86
```

<details>
<summary><strong>Solusi Challenge</strong></summary>

```python
nama = "Rafi"
berat = 70  # kg
tinggi = 1.75  # meter

bmi = berat / (tinggi ** 2)

print(f"Nama: {nama}")
print(f"Berat: {berat} kg")
print(f"Tinggi: {tinggi} m")
print(f"BMI: {bmi:.2f}")  # :.2f = 2 desimal
```
</details>

---

## Resources

**Baca lebih lanjut** (optional):
- [Python Official Tutorial - Variables](https://docs.python.org/3/tutorial/introduction.html#using-python-as-a-calculator)
- [PEP 8 - Style Guide for Python](https://pep8.org/) (naming convention resmi)

**Stuck?** Tanya di [Discord Community](../../resources/community.md).

Ready buat Lesson 2? Let's go! 🚀
