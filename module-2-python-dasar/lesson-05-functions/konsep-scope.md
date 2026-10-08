## Scope - Local vs Global

**Scope** = dimana variable bisa diakses.

---

### Local Scope

Variable di dalam function = **local**. Ga bisa diakses dari luar.

```python
def test():
    x = 10  # local
    print(x)

test()  # 10
print(x)  # ❌ Error: x is not defined
```

---

### Global Scope

Variable di luar function = **global**. Bisa diakses dari mana aja.

```python
x = 10  # global

def test():
    print(x)  # bisa akses global

test()  # 10
print(x)  # 10
```

---

### Modify Global Variable

**❌ Ini ga modify global**:

```python
x = 10

def test():
    x = 20  # bikin local variable baru, ga ganti global
    print(x)

test()  # 20
print(x)  # 10 (global ga berubah)
```

**✅ Pake keyword `global`**:

```python
x = 10

def test():
    global x
    x = 20  # modify global
    print(x)

test()  # 20
print(x)  # 20 (global berubah)
```

**Best practice**: **Hindari global**. Pass parameter instead.

```python
# ✅ Better
def tambah(x, y):
    return x + y

result = tambah(10, 5)
```

---

### Nested Function

Function dalam function.

```python
def outer():
    x = 10
    
    def inner():
        print(x)  # bisa akses x dari outer
    
    inner()

outer()  # 10
```

**nonlocal**: modify variable dari outer function.

```python
def outer():
    x = 10
    
    def inner():
        nonlocal x
        x = 20
    
    inner()
    print(x)  # 20

outer()
```

---

Next: ***args & **kwargs**.
