## Exercises - Loops

Praktek for, while, loop control, nested loops.

---

### Exercise 1: FizzBuzz

**Tujuan**: Classic programming test.

**Rules**:
- Print angka 1-100
- Kalau habis dibagi 3 → print "Fizz"
- Kalau habis dibagi 5 → print "Buzz"
- Kalau habis dibagi 3 DAN 5 → print "FizzBuzz"
- Kalau bukan keduanya → print angka

**Expected Output**:
```
1
2
Fizz
4
Buzz
Fizz
7
...
14
FizzBuzz
16
...
```

**Starter Code**:
```python
for i in range(1, 101):
    # Your code here
    pass
```

**Hint**: Cek 15 dulu (habis bagi 3 dan 5), baru cek 3, baru cek 5.

---

### Exercise 2: Multiplication Table

**Tujuan**: Print tabel perkalian 1-10.

**Expected Output**:
```
1 x 1 = 1    1 x 2 = 2    ... 1 x 10 = 10
2 x 1 = 2    2 x 2 = 4    ... 2 x 10 = 20
...
10 x 1 = 10  10 x 2 = 20  ... 10 x 10 = 100
```

**Starter Code**:
```python
for i in range(1, 11):
    for j in range(1, 11):
        # Your code here
        pass
```

---

### Exercise 3: Prime Numbers

**Tujuan**: Cari semua bilangan prima 2-50.

**Definisi**: Bilangan prima = cuma bisa dibagi 1 dan dirinya sendiri.

**Expected Output**:
```
[2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47]
```

**Starter Code**:
```python
primes = []

for num in range(2, 51):
    is_prime = True
    
    # Check if num is divisible by any number from 2 to num-1
    for i in range(2, num):
        if num % i == 0:
            is_prime = False
            break
    
    if is_prime:
        primes.append(num)

print(primes)
```

---

### Exercise 4: Password Validator

**Tujuan**: Loop sampe user input password yang valid.

**Rules**:
- Min 8 karakter
- Ada huruf besar
- Ada huruf kecil
- Ada angka

**Starter Code**:
```python
while True:
    password = input("Masukkan password: ")
    
    # Validasi
    if len(password) < 8:
        print("❌ Min 8 karakter")
        continue
    
    has_upper = any(c.isupper() for c in password)
    has_lower = any(c.islower() for c in password)
    has_digit = any(c.isdigit() for c in password)
    
    if not has_upper:
        print("❌ Harus ada huruf besar")
        continue
    
    if not has_lower:
        print("❌ Harus ada huruf kecil")
        continue
    
    if not has_digit:
        print("❌ Harus ada angka")
        continue
    
    print("✅ Password valid!")
    break
```

---

### Exercise 5: Pattern Generator

**Tujuan**: Print pattern berbagai bentuk.

**Pattern 1: Right Triangle**
```
*
**
***
****
*****
```

**Pattern 2: Inverted Triangle**
```
*****
****
***
**
*
```

**Pattern 3: Pyramid**
```
    *
   ***
  *****
 *******
*********
```

**Starter Code**:
```python
# Right Triangle
for i in range(1, 6):
    print("*" * i)

# Inverted
for i in range(5, 0, -1):
    print("*" * i)

# Pyramid
n = 5
for i in range(n):
    spaces = " " * (n - i - 1)
    stars = "*" * (2 * i + 1)
    print(spaces + stars)
```

---

## Bonus Challenge: Todo List CLI

**Tujuan**: Bikin simple todo list dengan menu loop.

**Features**:
- Tambah task
- Lihat semua tasks
- Hapus task
- Keluar

**Starter Code**:
```python
tasks = []

while True:
    print("\n=== Todo List ===")
    print("1. Tambah task")
    print("2. Lihat tasks")
    print("3. Hapus task")
    print("4. Keluar")
    
    pilihan = input("Pilih (1-4): ")
    
    if pilihan == "1":
        task = input("Task baru: ")
        tasks.append(task)
        print("✅ Task ditambah")
    
    elif pilihan == "2":
        if not tasks:
            print("Ga ada task")
        else:
            for i, task in enumerate(tasks, start=1):
                print(f"{i}. {task}")
    
    elif pilihan == "3":
        # Your code: hapus task by index
        pass
    
    elif pilihan == "4":
        print("Bye!")
        break
    
    else:
        print("Pilihan ga valid")
```

---

## Checklist

- [ ] FizzBuzz works 1-100
- [ ] Multiplication table formatted
- [ ] Prime numbers correct
- [ ] Password validator loops sampe valid
- [ ] Pattern prints correctly

---

Next: **Summary** - recap Loops!
