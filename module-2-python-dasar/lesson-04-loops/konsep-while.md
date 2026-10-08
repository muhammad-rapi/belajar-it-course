## While Loop

While loop = loop **selama kondisi True**.

---

### Syntax

```python
while kondisi:
    # do something
```

Loop jalan terus sampe kondisi jadi False.

---

### Contoh Simple

```python
count = 0

while count < 5:
    print(count)
    count += 1  # increment, wajib biar ga infinite loop
```

Output:
```
0
1
2
3
4
```

**Penjelasan**:
1. count = 0, cek 0 < 5? Yes → print 0, count jadi 1
2. count = 1, cek 1 < 5? Yes → print 1, count jadi 2
3. ... sampe count = 5
4. count = 5, cek 5 < 5? No → stop

---

### For vs While

**For** = lu tau berapa kali loop (iterate list, range, dll)  
**While** = lu ga tau berapa kali, loop sampe kondisi tertentu

**Contoh**: Tebak angka sampe bener.

```python
rahasia = 7
tebakan = 0

while tebakan != rahasia:
    tebakan = int(input("Tebak angka: "))
    
    if tebakan < rahasia:
        print("Terlalu kecil")
    elif tebakan > rahasia:
        print("Terlalu besar")
    else:
        print("Benar! 🎉")
```

Lu ga tau user butuh berapa kali tebak. Makanya pake while.

---

### Infinite Loop (Hati-Hati!)

Kalau kondisi ga pernah False, loop jalan selamanya.

```python
# ⚠️ JANGAN JALANIN INI
while True:
    print("Infinite loop!")
```

Komputer hang. Harus force quit.

**Fix**: Pastikan ada cara buat kondisi jadi False.

```python
count = 0

while True:
    print(count)
    count += 1
    
    if count >= 5:
        break  # stop loop
```

---

### Contoh Real: Validasi Input

```python
umur = -1

while umur < 0 or umur > 120:
    umur = int(input("Masukkan umur (0-120): "))
    
    if umur < 0 or umur > 120:
        print("Umur ga valid, coba lagi")

print(f"Umur lu: {umur}")
```

Loop jalan terus sampe user input valid.

---

### Contoh Real: Menu Loop

```python
while True:
    print("\n=== Menu ===")
    print("1. Tambah data")
    print("2. Lihat data")
    print("3. Keluar")
    
    pilihan = input("Pilih (1-3): ")
    
    if pilihan == "1":
        print("Tambah data...")
    elif pilihan == "2":
        print("Lihat data...")
    elif pilihan == "3":
        print("Bye!")
        break  # keluar loop
    else:
        print("Pilihan ga valid")
```

Program jalan terus sampe user pilih "3" (keluar).

---

### While dengan Else

Jarang dipake, tapi ada.

```python
count = 0

while count < 3:
    print(count)
    count += 1
else:
    print("Loop selesai normal")  # jalan kalau loop ga di-break
```

Output:
```
0
1
2
Loop selesai normal
```

**Dengan break**:

```python
count = 0

while count < 5:
    print(count)
    if count == 2:
        break
    count += 1
else:
    print("Ini ga jalan karena loop di-break")
```

Output:
```
0
1
2
```

Else **ga jalan** kalau loop di-break.

---

Next: **Loop Control** - break, continue, pass.
