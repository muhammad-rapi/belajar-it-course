## Define Function

### Syntax

```python
def nama_function(parameter1, parameter2):
    # code
    return result
```

**def** = define  
**nama_function** = kasih nama deskriptif  
**parameters** = input (optional)  
**return** = output (optional)

---

### Function Tanpa Parameter & Return

```python
def sapa():
    print("Halo!")

sapa()  # Halo!
```

---

### Function dengan Parameter

```python
def sapa(nama):
    print(f"Halo, {nama}!")

sapa("Rafi")  # Halo, Rafi!
sapa("Budi")  # Halo, Budi!
```

**Parameter** = variable di definisi function  
**Argument** = value yang lu pass waktu call function

---

### Function dengan Return

```python
def tambah(a, b):
    return a + b

hasil = tambah(5, 3)
print(hasil)  # 8
```

**return** = kasih value balik ke caller.

Tanpa return, function return `None`:

```python
def test():
    print("Hello")

result = test()  # Hello
print(result)    # None
```

---

### Multiple Parameters

```python
def info_user(nama, umur, kota):
    print(f"{nama}, {umur} tahun, tinggal di {kota}")

info_user("Rafi", 25, "Jakarta")
# Rafi, 25 tahun, tinggal di Jakarta
```

---

### Default Parameter

```python
def sapa(nama, salam="Halo"):
    print(f"{salam}, {nama}!")

sapa("Rafi")              # Halo, Rafi!
sapa("Rafi", "Hi")        # Hi, Rafi!
sapa("Rafi", salam="Yo") # Yo, Rafi!
```

Default parameter **harus di akhir**:

```python
# ✅ OK
def func(a, b, c=10):
    pass

# ❌ Error
def func(a, b=10, c):
    pass
```

---

### Return Multiple Values

```python
def hitung(a, b):
    jumlah = a + b
    selisih = a - b
    return jumlah, selisih

hasil1, hasil2 = hitung(10, 5)
print(hasil1)  # 15
print(hasil2)  # 5
```

Sebenernya return **tuple**.

---

### Docstring

Dokumentasi function.

```python
def tambah(a, b):
    """
    Tambahkan 2 angka.
    
    Args:
        a (int): Angka pertama
        b (int): Angka kedua
    
    Returns:
        int: Hasil penjumlahan
    """
    return a + b

# Check docstring
print(tambah.__doc__)
```

---

Next: **Scope** - local vs global variables.
