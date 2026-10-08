## Nested Loops

Nested loop = **loop dalam loop**.

---

### Syntax

```python
for i in outer:
    for j in inner:
        # do something
```

**Outer loop** jalan 1x → **inner loop** jalan lengkap → outer loop lanjut.

---

### Contoh Simple

```python
for i in range(1, 4):  # outer
    for j in range(1, 4):  # inner
        print(f"i={i}, j={j}")
```

Output:
```
i=1, j=1
i=1, j=2
i=1, j=3
i=2, j=1
i=2, j=2
i=2, j=3
i=3, j=1
i=3, j=2
i=3, j=3
```

**Penjelasan**:
1. i=1 → inner loop jalan 3x (j=1, j=2, j=3)
2. i=2 → inner loop jalan 3x lagi
3. i=3 → inner loop jalan 3x lagi

**Total**: 3 x 3 = 9 iterasi.

---

### Contoh: Multiplication Table

```python
for i in range(1, 6):
    for j in range(1, 6):
        print(f"{i} x {j} = {i*j}")
    print()  # blank line tiap outer loop
```

Output:
```
1 x 1 = 1
1 x 2 = 2
...
5 x 5 = 25
```

---

### Contoh: Pattern Printing

**Triangle**:

```python
for i in range(1, 6):
    for j in range(i):
        print("*", end="")
    print()  # new line
```

Output:
```
*
**
***
****
*****
```

**Square**:

```python
for i in range(5):
    for j in range(5):
        print("#", end=" ")
    print()
```

Output:
```
# # # # # 
# # # # # 
# # # # # 
# # # # # 
# # # # # 
```

---

### Contoh Real: Nested List (Matrix)

```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

for row in matrix:
    for item in row:
        print(item, end=" ")
    print()
```

Output:
```
1 2 3 
4 5 6 
7 8 9 
```

---

### Contoh Real: Kombinasi

```python
warna = ["merah", "hijau", "biru"]
ukuran = ["S", "M", "L"]

produk = []

for w in warna:
    for u in ukuran:
        produk.append(f"{w}-{u}")

print(produk)
```

Output:
```
['merah-S', 'merah-M', 'merah-L', 
 'hijau-S', 'hijau-M', 'hijau-L', 
 'biru-S', 'biru-M', 'biru-L']
```

3 warna x 3 ukuran = 9 kombinasi.

---

### Performance Warning

Nested loop = **exponential time**.

```python
# O(n²)
for i in range(1000):      # 1000x
    for j in range(1000):  # 1000x
        print(i, j)        # Total: 1,000,000x
```

**1 juta iterasi**. Lambat.

**3 nested loops**:

```python
# O(n³)
for i in range(100):    # 100x
    for j in range(100):  # 100x
        for k in range(100):  # 100x
            pass  # Total: 1,000,000x
```

**Rule**: Hindari nested loop > 2 level kalau ga perlu. Cari algoritma lain.

---

### Break di Nested Loop

**break** cuma keluar dari inner loop, bukan outer.

```python
for i in range(3):
    for j in range(3):
        if j == 1:
            break  # keluar inner loop doang
        print(f"i={i}, j={j}")
```

Output:
```
i=0, j=0
i=1, j=0
i=2, j=0
```

**Break outer loop**: pake flag.

```python
found = False

for i in range(3):
    for j in range(3):
        if i == 1 and j == 1:
            found = True
            break
    if found:
        break
```

Atau extract ke function, pake `return`.

---

Next: **Exercises** - praktek loops!
