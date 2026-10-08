## Summary - Data Types & Operations

Selamat! Lu udah paham cara Python simpen dan manipulasi berbagai jenis data.

---

## Yang Udah Lu Pelajari

### 1. String Operations
- Methods: `.upper()`, `.lower()`, `.strip()`, `.replace()`, `.split()`, `.join()`
- Slicing: `text[0:5]`
- F-string: `f"Hello {nama}"`
- String immutable (ga bisa diubah langsung)

### 2. Lists
- Bikin list: `buah = ["apel", "jeruk"]`
- Akses: `buah[0]` (index dimulai dari 0)
- Tambah: `.append()`, `.insert()`
- Hapus: `.remove()`, `.pop()`
- Loop: `for item in list:`
- Methods: `.sort()`, `.reverse()`, `len()`, `max()`, `min()`

### 3. Dictionaries
- Bikin dict: `user = {"nama": "Rafi", "umur": 25}`
- Akses: `user["nama"]` atau `user.get("nama")`
- Tambah/update: `user["email"] = "..."`
- Hapus: `del user["key"]` atau `user.pop("key")`
- Loop: `for key, value in dict.items():`
- Check: `"nama" in user`

### 4. Type Conversion
- `int()` - Convert ke integer
- `float()` - Convert ke float
- `str()` - Convert ke string
- `bool()` - Convert ke boolean
- `type()` - Check tipe data

---

## Skill yang Lu Kuasai Sekarang

✅ Manipulasi text (uppercase, lowercase, split, join)  
✅ Simpen banyak data dalam list  
✅ Simpen data terstruktur dalam dictionary  
✅ Convert antar tipe data  
✅ Handle input user (string → int/float)  
✅ Loop list dan dictionary  

---

## Pattern yang Sering Dipake

**1. Parse CSV/text**

```python
data = "Rafi,25,Jakarta"
parts = data.split(",")
nama = parts[0]
umur = int(parts[1])
```

**2. Build string dari list**

```python
words = ["Aku", "suka", "Python"]
sentence = " ".join(words)  # "Aku suka Python"
```

**3. List of dictionaries (data collection)**

```python
users = [
    {"nama": "Rafi", "umur": 25},
    {"nama": "Budi", "umur": 30}
]

for user in users:
    print(f"{user['nama']} - {user['umur']} tahun")
```

**4. Safe input conversion**

```python
input_user = input("Umur: ")
if input_user.isdigit():
    umur = int(input_user)
else:
    print("Input harus angka")
```

---

## Comparison: List vs Dictionary

| Aspek | List | Dictionary |
|-------|------|------------|
| **Structure** | Ordered, index-based | Key-value pairs |
| **Akses** | `list[0]` | `dict["key"]` |
| **Use case** | Kumpulan item sejenis | Data terstruktur |
| **Contoh** | `["apel", "jeruk"]` | `{"nama": "Rafi"}` |

**Kapan pake list?** Kalau cuma butuh kumpulan data (nama-nama, angka-angka).

**Kapan pake dictionary?** Kalau data punya attribute/property (user punya nama, umur, email).

---

## Next Steps

**Next lesson: Conditionals (If-Else)** - bikin keputusan berdasarkan data.

Preview:

```python
nama = "Rafi"

if nama in ["Rafi", "Budi", "Siti"]:
    print("Nama terdaftar")
else:
    print("Nama tidak ditemukan")

# Grade dari nilai
nilai = 85
if nilai >= 80:
    grade = "B"
else:
    grade = "C"
```

Sebelum lanjut, **pastiin lu udah**:
- [ ] Ngerjain semua 5 exercises
- [ ] Paham perbedaan list vs dictionary
- [ ] Bisa manipulasi string dasar
- [ ] Bisa convert string → int/float

---

## Tips Praktis

**1. String formatting**

```python
# ✅ Modern (f-string)
nama = "Rafi"
umur = 25
print(f"Nama: {nama}, Umur: {umur}")

# ❌ Old (concatenation)
print("Nama: " + nama + ", Umur: " + str(umur))
```

**2. Check empty**

```python
# List/dict empty?
if not my_list:
    print("List kosong")

if not my_dict:
    print("Dict kosong")
```

**3. List comprehension (preview advanced)**

```python
# Biasa
squares = []
for i in range(5):
    squares.append(i ** 2)

# List comprehension (lebih singkat)
squares = [i ** 2 for i in range(5)]
```

---

## Common Gotchas (Jebakan)

**1. String vs List**

```python
text = "hello"
print(text[0])  # 'h' (string juga bisa indexing)

# String immutable
text[0] = "H"  # ❌ Error

# List mutable
my_list = ["h", "e", "l", "l", "o"]
my_list[0] = "H"  # ✅ Jalan
```

**2. Dict key typo**

```python
user = {"nama": "Rafi"}
print(user["name"])  # ❌ KeyError (typo: "name" vs "nama")

# Lebih aman pake .get()
print(user.get("name"))  # None (ga error)
```

**3. Lupa convert input**

```python
umur = input("Umur: ")  # String!
if umur > 18:  # ❌ Compare string vs int
    print("Dewasa")

# Fix
umur = int(input("Umur: "))
```

---

## Challenge (Optional)

**Mini Project: Simple Phonebook**

Bikin phonebook dengan fitur:
1. Tambah contact
2. Cari contact by name
3. Update phone number
4. Delete contact
5. Show all contacts

<details>
<summary><strong>Starter Code</strong></summary>

```python
phonebook = []

# Tambah 3 contacts
phonebook.append({"nama": "Rafi", "phone": "0812..."})
phonebook.append({"nama": "Budi", "phone": "0813..."})
phonebook.append({"nama": "Siti", "phone": "0814..."})

# Print semua
for contact in phonebook:
    print(f"{contact['nama']}: {contact['phone']}")

# Cari "Budi"
for contact in phonebook:
    if contact["nama"] == "Budi":
        print(f"Found: {contact}")

# Update Siti's phone
for contact in phonebook:
    if contact["nama"] == "Siti":
        contact["phone"] = "0819..."

# Hapus Rafi
phonebook = [c for c in phonebook if c["nama"] != "Rafi"]
```
</details>

---

Ready buat Lesson 3 (Conditionals)? 🚀
