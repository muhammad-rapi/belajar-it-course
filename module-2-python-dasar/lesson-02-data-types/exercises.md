## Exercises - Data Types & Operations

Praktek manipulasi string, list, dictionary, dan type conversion.

---

### Exercise 1: String Manipulation

**Tujuan**: Bersihkan dan format data nama.

**Yang Perlu Lu Lakukan**:
1. Bikin file `nama_cleaner.py`
2. Set variable `nama` dengan value yang berantakan: `"  rafi MAULANA  "`
3. Bersihkan (strip spasi, title case)
4. Pisah jadi first name & last name
5. Print hasil

**Expected Output**:
```
Nama asli: "  rafi MAULANA  "
Nama bersih: "Rafi Maulana"
First name: Rafi
Last name: Maulana
```

<details>
<summary><strong>Hint</strong></summary>

```python
nama.strip()   # Buang spasi
nama.title()   # Title case
nama.split()   # Pecah jadi list
```
</details>

<details>
<summary><strong>Solusi</strong></summary>

```python
nama = "  rafi MAULANA  "

# Bersihkan
nama_bersih = nama.strip().title()

# Pisah
nama_list = nama_bersih.split()
first_name = nama_list[0]
last_name = nama_list[1]

print(f'Nama asli: "{nama}"')
print(f'Nama bersih: "{nama_bersih}"')
print(f"First name: {first_name}")
print(f"Last name: {last_name}")
```
</details>

---

### Exercise 2: Todo List Manager

**Tujuan**: Bikin dan manipulasi todo list.

**Yang Perlu Lu Lakukan**:
1. Bikin file `todo_list.py`
2. Bikin list kosong `todos`
3. Tambah 3 task
4. Print jumlah task
5. Mark task pertama sebagai done (tambahin "✓" di depan)
6. Hapus task terakhir
7. Print semua task

**Expected Output**:
```
Task: 3
1. ✓ Belajar Python
2. Bikin project
```

<details>
<summary><strong>Solusi</strong></summary>

```python
# Bikin list
todos = []

# Tambah task
todos.append("Belajar Python")
todos.append("Bikin project")
todos.append("Push ke GitHub")

print(f"Task: {len(todos)}")

# Mark done (update task pertama)
todos[0] = "✓ " + todos[0]

# Hapus task terakhir
todos.pop()

# Print semua
for i, task in enumerate(todos, 1):
    print(f"{i}. {task}")
```
</details>

---

### Exercise 3: User Profile Dictionary

**Tujuan**: Bikin dan update user profile.

**Yang Perlu Lu Lakukan**:
1. Bikin file `user_profile.py`
2. Bikin dictionary `user` dengan:
   - nama: "Rafi"
   - umur: 25
   - kota: "Jakarta"
3. Tambah key `email` dengan value "rafi@gmail.com"
4. Update `umur` jadi 26
5. Print semua data dalam format rapi

**Expected Output**:
```
=== User Profile ===
Nama: Rafi
Umur: 26
Kota: Jakarta
Email: rafi@gmail.com
```

<details>
<summary><strong>Solusi</strong></summary>

```python
# Bikin dictionary
user = {
    "nama": "Rafi",
    "umur": 25,
    "kota": "Jakarta"
}

# Tambah email
user["email"] = "rafi@gmail.com"

# Update umur
user["umur"] = 26

# Print rapi
print("=== User Profile ===")
for key, value in user.items():
    print(f"{key.capitalize()}: {value}")

# Atau manual:
# print(f"Nama: {user['nama']}")
# print(f"Umur: {user['umur']}")
# dll...
```
</details>

---

### Exercise 4: Simple Calculator (Type Conversion)

**Tujuan**: Bikin kalkulator yang terima input string, convert ke angka.

**Yang Perlu Lu Lakukan**:
1. Bikin file `calculator.py`
2. Set 2 variable input (anggap dari user, tapi lu hard-code dulu):
   - `angka1 = "15"`
   - `angka2 = "7"`
3. Convert ke int
4. Hitung: tambah, kurang, kali, bagi
5. Print hasil semua operasi

**Expected Output**:
```
15 + 7 = 22
15 - 7 = 8
15 * 7 = 105
15 / 7 = 2.14
```

<details>
<summary><strong>Hint</strong></summary>

```python
int(angka1)  # Convert string → int
```

Bagi hasilnya float, format pakai `:.2f` buat 2 desimal.
</details>

<details>
<summary><strong>Solusi</strong></summary>

```python
# Input (string)
angka1 = "15"
angka2 = "7"

# Convert ke int
num1 = int(angka1)
num2 = int(angka2)

# Hitung
tambah = num1 + num2
kurang = num1 - num2
kali = num1 * num2
bagi = num1 / num2

# Print
print(f"{num1} + {num2} = {tambah}")
print(f"{num1} - {num2} = {kurang}")
print(f"{num1} * {num2} = {kali}")
print(f"{num1} / {num2} = {bagi:.2f}")
```

**Bonus** (dengan input real):

```python
angka1 = input("Angka 1: ")
angka2 = input("Angka 2: ")

num1 = int(angka1)
num2 = int(angka2)

print(f"{num1} + {num2} = {num1 + num2}")
print(f"{num1} - {num2} = {num1 - num2}")
print(f"{num1} * {num2} = {num1 * num2}")
print(f"{num1} / {num2} = {num1 / num2:.2f}")
```
</details>

---

### Exercise 5: Challenge - Contact Manager

**Tujuan**: Bikin mini contact manager dengan list of dictionaries.

**Yang Perlu Lu Lakukan**:
1. Bikin file `contacts.py`
2. Bikin list `contacts` berisi 3 dictionary:
   - Contact 1: Rafi, 081234567890, rafi@gmail.com
   - Contact 2: Budi, 081298765432, budi@gmail.com
   - Contact 3: Siti, 081211112222, siti@gmail.com
3. Print semua contact dalam format rapi
4. Cari contact dengan nama "Budi" dan print detailnya
5. Update nomor HP Siti jadi "081299998888"

**Expected Output**:
```
=== All Contacts ===
1. Rafi
   Phone: 081234567890
   Email: rafi@gmail.com

2. Budi
   Phone: 081298765432
   Email: budi@gmail.com

3. Siti
   Phone: 081211112222
   Email: siti@gmail.com

=== Search: Budi ===
Nama: Budi
Phone: 081298765432
Email: budi@gmail.com

=== Update Siti's Phone ===
Siti's new phone: 081299998888
```

<details>
<summary><strong>Hint 1</strong></summary>

Structure:
```python
contacts = [
    {"nama": "Rafi", "phone": "...", "email": "..."},
    {"nama": "Budi", "phone": "...", "email": "..."},
    # ...
]
```
</details>

<details>
<summary><strong>Hint 2</strong></summary>

Loop contacts:
```python
for i, contact in enumerate(contacts, 1):
    print(f"{i}. {contact['nama']}")
```

Cari contact:
```python
for contact in contacts:
    if contact["nama"] == "Budi":
        print(contact)
```
</details>

<details>
<summary><strong>Solusi</strong></summary>

```python
# Bikin contacts
contacts = [
    {
        "nama": "Rafi",
        "phone": "081234567890",
        "email": "rafi@gmail.com"
    },
    {
        "nama": "Budi",
        "phone": "081298765432",
        "email": "budi@gmail.com"
    },
    {
        "nama": "Siti",
        "phone": "081211112222",
        "email": "siti@gmail.com"
    }
]

# Print semua
print("=== All Contacts ===")
for i, contact in enumerate(contacts, 1):
    print(f"{i}. {contact['nama']}")
    print(f"   Phone: {contact['phone']}")
    print(f"   Email: {contact['email']}")
    print()

# Cari Budi
print("=== Search: Budi ===")
for contact in contacts:
    if contact["nama"] == "Budi":
        print(f"Nama: {contact['nama']}")
        print(f"Phone: {contact['phone']}")
        print(f"Email: {contact['email']}")
        print()

# Update Siti's phone
print("=== Update Siti's Phone ===")
for contact in contacts:
    if contact["nama"] == "Siti":
        contact["phone"] = "081299998888"
        print(f"Siti's new phone: {contact['phone']}")
```
</details>

---

## Checklist

Abis ngerjain:
- [ ] Semua file jalan tanpa error
- [ ] Output sesuai expected
- [ ] Paham perbedaan list vs dictionary
- [ ] Bisa manipulasi string (strip, split, title, dll)
- [ ] Bisa convert tipe data

**Debug tips**:

```python
# Print tipe data
print(type(variable))

# Print isi list/dict
print(contacts)

# Print dengan format rapi
import json
print(json.dumps(contacts, indent=2))
```

---

Next: **Summary** - ringkasan lesson + next steps.
