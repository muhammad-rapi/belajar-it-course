## Lists - Array Python

List = kumpulan data **ordered** (ada urutan). Bisa simpen banyak item dalam 1 variable.

---

### Bikin List

```python
# List kosong
data = []

# List dengan data
buah = ["apel", "jeruk", "mangga"]
angka = [1, 2, 3, 4, 5]

# List bisa campur tipe data (tapi hindari, bikin bingung)
campur = ["Rafi", 25, True, 175.5]
```

---

### Akses Item (Indexing)

Index dimulai dari **0**:

```python
buah = ["apel", "jeruk", "mangga"]

print(buah[0])   # apel (index 0)
print(buah[1])   # jeruk
print(buah[2])   # mangga
print(buah[-1])  # mangga (index terakhir)
print(buah[-2])  # jeruk
```

---

### Ubah Item

```python
buah = ["apel", "jeruk", "mangga"]
buah[1] = "semangka"  # Ganti "jeruk" jadi "semangka"

print(buah)  # ['apel', 'semangka', 'mangga']
```

---

### Tambah Item

```python
buah = ["apel", "jeruk"]

# Tambah di akhir
buah.append("mangga")
print(buah)  # ['apel', 'jeruk', 'mangga']

# Tambah di index tertentu
buah.insert(1, "pisang")  # Tambah di index 1
print(buah)  # ['apel', 'pisang', 'jeruk', 'mangga']
```

---

### Hapus Item

```python
buah = ["apel", "jeruk", "mangga"]

# Hapus by value
buah.remove("jeruk")
print(buah)  # ['apel', 'mangga']

# Hapus by index
buah = ["apel", "jeruk", "mangga"]
buah.pop(1)  # Hapus index 1
print(buah)  # ['apel', 'mangga']

# Hapus semua
buah.clear()
print(buah)  # []
```

---

### Loop (Preview - detail di Lesson 4)

```python
buah = ["apel", "jeruk", "mangga"]

for item in buah:
    print(item)

# Output:
# apel
# jeruk
# mangga
```

---

### List Methods

```python
angka = [3, 1, 4, 1, 5, 9]

print(len(angka))      # 6 (panjang list)
print(max(angka))      # 9 (nilai terbesar)
print(min(angka))      # 1 (nilai terkecil)
print(sum(angka))      # 23 (total)
print(angka.count(1))  # 2 (berapa kali 1 muncul)

angka.sort()           # Sort ascending
print(angka)           # [1, 1, 3, 4, 5, 9]

angka.reverse()        # Balik urutan
print(angka)           # [9, 5, 4, 3, 1, 1]
```

---

### List Slicing

```python
angka = [0, 1, 2, 3, 4, 5]

print(angka[1:4])   # [1, 2, 3] (index 1-3)
print(angka[:3])    # [0, 1, 2] (awal sampai index 2)
print(angka[3:])    # [3, 4, 5] (index 3 sampai akhir)
print(angka[::2])   # [0, 2, 4] (skip 1)
```

---

### Check Item Ada Ga

```python
buah = ["apel", "jeruk", "mangga"]

print("apel" in buah)     # True
print("pisang" in buah)   # False
```

---

## Contoh Praktis

**Use case 1: Todo list**

```python
todo = []
todo.append("Belajar Python")
todo.append("Bikin project")
todo.append("Push ke GitHub")

print(f"Kamu punya {len(todo)} task:")
for task in todo:
    print(f"- {task}")
```

**Use case 2: Pisah nama**

```python
nama_lengkap = "Rafi Maulana Hidayat"
nama_list = nama_lengkap.split(" ")

first_name = nama_list[0]
last_name = nama_list[-1]

print(f"First: {first_name}")  # Rafi
print(f"Last: {last_name}")    # Hidayat
```

---

Next: **Dictionaries** - data terstruktur key-value.
