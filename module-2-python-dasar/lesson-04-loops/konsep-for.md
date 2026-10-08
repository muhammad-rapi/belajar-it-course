## For Loop

For loop = **iterate** (lewatin satu-satu) items di collection (list, range, string, dll).

---

### Syntax

```python
for item in collection:
    # do something
```

---

### Loop List

```python
buah = ["apel", "mangga", "jeruk"]

for b in buah:
    print(b)
```

Output:
```
apel
mangga
jeruk
```

**Analogi**: Lu punya tumpukan kartu. Lu ambil satu-satu dari atas, baca, terus lanjut ke kartu berikutnya.

---

### Loop Range

**range(start, stop, step)** = generate angka.

**range(5)** → 0, 1, 2, 3, 4

```python
for i in range(5):
    print(i)
```

Output:
```
0
1
2
3
4
```

**range(1, 6)** → 1, 2, 3, 4, 5

```python
for i in range(1, 6):
    print(i)
```

**range(0, 10, 2)** → 0, 2, 4, 6, 8 (step 2)

```python
for i in range(0, 10, 2):
    print(i)
```

---

### Loop String

String = collection of characters.

```python
nama = "Rafi"

for huruf in nama:
    print(huruf)
```

Output:
```
R
a
f
i
```

---

### Loop dengan Index

Kadang lu butuh index (posisi).

**enumerate()** = kasih index + value.

```python
buah = ["apel", "mangga", "jeruk"]

for index, b in enumerate(buah):
    print(f"{index}: {b}")
```

Output:
```
0: apel
1: mangga
2: jeruk
```

**Start index dari 1**:

```python
for index, b in enumerate(buah, start=1):
    print(f"{index}. {b}")
```

Output:
```
1. apel
2. mangga
3. jeruk
```

---

### Loop Dictionary

**Loop keys**:

```python
user = {"name": "Rafi", "age": 25}

for key in user:
    print(key)
```

Output:
```
name
age
```

**Loop values**:

```python
for value in user.values():
    print(value)
```

Output:
```
Rafi
25
```

**Loop key + value**:

```python
for key, value in user.items():
    print(f"{key}: {value}")
```

Output:
```
name: Rafi
age: 25
```

---

### Contoh Real: Sum Numbers

```python
numbers = [10, 20, 30, 40, 50]
total = 0

for num in numbers:
    total += num  # total = total + num

print(f"Total: {total}")  # 150
```

---

### Contoh Real: Filter Even Numbers

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
even = []

for num in numbers:
    if num % 2 == 0:
        even.append(num)

print(even)  # [2, 4, 6, 8, 10]
```

---

Next: **While Loop** - loop dengan kondisi.
