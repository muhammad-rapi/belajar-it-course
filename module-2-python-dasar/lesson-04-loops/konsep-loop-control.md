## Loop Control - break, continue, pass

3 keyword buat kontrol loop flow.

---

### break - Stop Loop

**break** = keluar dari loop sekarang juga.

```python
for i in range(10):
    if i == 5:
        break  # stop di 5
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

Loop stop di 5, ga lanjut ke 6-9.

**Contoh real**: Cari item di list.

```python
users = ["Rafi", "Budi", "Siti", "Joko"]
target = "Siti"

for user in users:
    if user == target:
        print(f"Ketemu: {user}")
        break  # ga perlu cek sisanya

# Output: Ketemu: Siti
```

Efisien. Ga buang waktu cek "Joko" kalau udah ketemu "Siti".

---

### continue - Skip ke Iterasi Berikutnya

**continue** = skip code dibawahnya, lanjut ke iterasi berikutnya.

```python
for i in range(5):
    if i == 2:
        continue  # skip print kalau i = 2
    print(i)
```

Output:
```
0
1
3
4
```

Angka 2 di-skip.

**Contoh real**: Skip invalid data.

```python
numbers = [10, -5, 20, -3, 30]

for num in numbers:
    if num < 0:
        continue  # skip negative
    print(num)
```

Output:
```
10
20
30
```

---

### pass - Placeholder

**pass** = ga ngapa-ngapain. Placeholder buat code yang belum ditulis.

```python
for i in range(5):
    if i == 2:
        pass  # TODO: implementasi nanti
    else:
        print(i)
```

Output:
```
0
1
3
4
```

**Kenapa perlu pass?**

Python ga boleh ada block kosong. Kalau belum tau mau ngapain, pake pass.

```python
# ❌ Error
for i in range(5):
    if i == 2:
        # Kosong, error!

# ✅ OK
for i in range(5):
    if i == 2:
        pass  # Placeholder
```

**Real use case**: Lagi bikin app, belum tau logic-nya.

```python
def process_payment(amount):
    pass  # TODO: integrate payment gateway

def send_email(to, subject, body):
    pass  # TODO: setup SMTP
```

Code bisa jalan tanpa error, tinggal implementasi nanti.

---

### break vs continue vs pass

| Keyword | Fungsi | Kapan Pake |
|---------|--------|------------|
| `break` | Stop loop | Udah dapet yang dicari |
| `continue` | Skip ke next iteration | Skip invalid data |
| `pass` | Do nothing | Placeholder |

---

### Contoh Kombinasi

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

for num in numbers:
    if num > 7:
        break  # stop kalau > 7
    
    if num % 2 == 0:
        continue  # skip genap
    
    print(num)
```

Output:
```
1
3
5
7
```

**Penjelasan**:
- 1, 3, 5, 7 → print (ganjil & ≤ 7)
- 2, 4, 6 → skip (genap)
- 8 → break (> 7), loop stop

---

Next: **Nested Loops** - loop dalam loop.
