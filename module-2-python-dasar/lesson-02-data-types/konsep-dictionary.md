## Dictionaries - Key-Value Data

Dictionary = data **key-value**. Kayak kamus (key = kata, value = arti).

---

### Kenapa Pakai Dictionary?

**Tanpa dictionary** (ribet):

```python
user1_nama = "Rafi"
user1_umur = 25
user1_kota = "Jakarta"

user2_nama = "Budi"
user2_umur = 30
user2_kota = "Bandung"
```

**Dengan dictionary** (rapi):

```python
user1 = {
    "nama": "Rafi",
    "umur": 25,
    "kota": "Jakarta"
}

user2 = {
    "nama": "Budi",
    "umur": 30,
    "kota": "Bandung"
}
```

---

### Bikin Dictionary

```python
# Kosong
data = {}

# Dengan data
user = {
    "nama": "Rafi",
    "umur": 25,
    "kota": "Jakarta",
    "hobi": ["coding", "gaming", "reading"]
}
```

**Key** harus string atau number. **Value** bisa tipe apa aja (string, int, list, bahkan dictionary lain).

---

### Akses Value

```python
user = {
    "nama": "Rafi",
    "umur": 25
}

print(user["nama"])  # Rafi
print(user["umur"])  # 25

# Atau pake .get() (lebih aman)
print(user.get("nama"))  # Rafi
print(user.get("email"))  # None (ga error kalau key ga ada)
```

**Perbedaan `[]` vs `.get()`**:

```python
print(user["email"])      # ❌ KeyError (error kalau key ga ada)
print(user.get("email"))  # ✅ None (ga error, return None)
```

---

### Tambah / Update Value

```python
user = {
    "nama": "Rafi",
    "umur": 25
}

# Tambah key baru
user["email"] = "rafi@gmail.com"

# Update value yang udah ada
user["umur"] = 26

print(user)
# {'nama': 'Rafi', 'umur': 26, 'email': 'rafi@gmail.com'}
```

---

### Hapus Key

```python
user = {
    "nama": "Rafi",
    "umur": 25,
    "kota": "Jakarta"
}

# Hapus key
del user["kota"]

# Atau pake .pop()
umur = user.pop("umur")  # Hapus dan return value-nya
print(umur)  # 25
print(user)  # {'nama': 'Rafi'}
```

---

### Loop Dictionary

```python
user = {
    "nama": "Rafi",
    "umur": 25,
    "kota": "Jakarta"
}

# Loop keys
for key in user:
    print(key)
# nama
# umur
# kota

# Loop keys + values
for key, value in user.items():
    print(f"{key}: {value}")
# nama: Rafi
# umur: 25
# kota: Jakarta
```

---

### Dictionary Methods

```python
user = {
    "nama": "Rafi",
    "umur": 25
}

print(user.keys())    # dict_keys(['nama', 'umur'])
print(user.values())  # dict_values(['Rafi', 25])
print(user.items())   # dict_items([('nama', 'Rafi'), ('umur', 25)])

print(len(user))      # 2 (jumlah key)
print("nama" in user) # True
```

---

### Nested Dictionary

Dictionary di dalam dictionary:

```python
users = {
    "user1": {
        "nama": "Rafi",
        "umur": 25
    },
    "user2": {
        "nama": "Budi",
        "umur": 30
    }
}

print(users["user1"]["nama"])  # Rafi
print(users["user2"]["umur"])  # 30
```

---

### List of Dictionaries

Pattern paling sering:

```python
users = [
    {"nama": "Rafi", "umur": 25},
    {"nama": "Budi", "umur": 30},
    {"nama": "Siti", "umur": 22}
]

# Loop
for user in users:
    print(f"{user['nama']} - {user['umur']} tahun")

# Output:
# Rafi - 25 tahun
# Budi - 30 tahun
# Siti - 22 tahun
```

---

## Contoh Praktis

**Use case: Config app**

```python
config = {
    "app_name": "Todo App",
    "version": "1.0",
    "debug": True,
    "database": {
        "host": "localhost",
        "port": 5432,
        "name": "todo_db"
    }
}

print(f"App: {config['app_name']} v{config['version']}")
print(f"DB: {config['database']['name']}")
```

**Use case: API response**

```python
# Hasil dari API (misal: user profile)
response = {
    "status": "success",
    "data": {
        "id": 123,
        "username": "rafi_dev",
        "followers": 1500,
        "verified": True
    }
}

if response["status"] == "success":
    user = response["data"]
    print(f"@{user['username']} - {user['followers']} followers")
```

---

Next: **Type Conversion** - ubah tipe data.
