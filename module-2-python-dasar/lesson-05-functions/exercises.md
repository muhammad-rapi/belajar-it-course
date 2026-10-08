## Exercises - Functions

Praktek define functions, scope, args/kwargs, lambda.

---

### Exercise 1: Calculator

**Tujuan**: Bikin calculator dengan functions.

**Features**: tambah, kurang, kali, bagi.

**Starter Code**:
```python
def tambah(a, b):
    return a + b

def kurang(a, b):
    return a - b

def kali(a, b):
    return a * b

def bagi(a, b):
    if b == 0:
        return "Error: Ga bisa bagi 0"
    return a / b

# Test
print(tambah(10, 5))  # 15
print(bagi(10, 0))    # Error: Ga bisa bagi 0
```

---

### Exercise 2: Temperature Converter

**Tujuan**: Convert suhu Celsius ↔ Fahrenheit.

**Formula**:
- C → F: (C × 9/5) + 32
- F → C: (F - 32) × 5/9

**Starter Code**:
```python
def celsius_to_fahrenheit(c):
    return (c * 9/5) + 32

def fahrenheit_to_celsius(f):
    return (f - 32) * 5/9

# Test
print(celsius_to_fahrenheit(0))   # 32.0
print(fahrenheit_to_celsius(32))  # 0.0
```

---

### Exercise 3: Palindrome Checker

**Tujuan**: Check apakah string palindrome (baca maju/mundur sama).

**Contoh**: "katak", "radar", "level" → palindrome.

**Starter Code**:
```python
def is_palindrome(text):
    text = text.lower().replace(" ", "")
    return text == text[::-1]

# Test
print(is_palindrome("katak"))     # True
print(is_palindrome("hello"))     # False
print(is_palindrome("A man a plan a canal Panama"))  # True
```

---

### Exercise 4: Grade Calculator

**Tujuan**: Hitung rata-rata nilai + grade.

**Grade**:
- 90-100 → A
- 80-89 → B
- 70-79 → C
- 60-69 → D
- < 60 → E

**Starter Code**:
```python
def hitung_grade(nilai_list):
    rata = sum(nilai_list) / len(nilai_list)
    
    if rata >= 90:
        grade = "A"
    elif rata >= 80:
        grade = "B"
    elif rata >= 70:
        grade = "C"
    elif rata >= 60:
        grade = "D"
    else:
        grade = "E"
    
    return rata, grade

# Test
rata, grade = hitung_grade([85, 90, 78, 92])
print(f"Rata-rata: {rata}, Grade: {grade}")
# Rata-rata: 86.25, Grade: B
```

---

### Exercise 5: *args & **kwargs

**Tujuan**: Bikin function yang terima variable arguments.

**Task 1**: Function yang terima berapa aja angka, return max.

```python
def find_max(*args):
    return max(args)

print(find_max(10, 5, 20, 15))  # 20
```

**Task 2**: Function yang print user info dari kwargs.

```python
def print_user(**kwargs):
    for key, value in kwargs.items():
        print(f"{key.capitalize()}: {value}")

print_user(name="Rafi", age=25, city="Jakarta")
# Name: Rafi
# Age: 25
# City: Jakarta
```

---

## Bonus Challenge: Fibonacci Generator

**Tujuan**: Generate Fibonacci sequence.

**Fibonacci**: 0, 1, 1, 2, 3, 5, 8, 13, ...  
(tiap angka = jumlah 2 angka sebelumnya)

**Starter Code**:
```python
def fibonacci(n):
    """Generate n angka Fibonacci pertama"""
    if n <= 0:
        return []
    elif n == 1:
        return [0]
    
    fib = [0, 1]
    for i in range(2, n):
        fib.append(fib[-1] + fib[-2])
    
    return fib

print(fibonacci(10))
# [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
```

---

## Checklist

- [ ] Calculator functions work
- [ ] Temperature converter correct
- [ ] Palindrome checker handles edge cases
- [ ] Grade calculator returns correct grade
- [ ] Fibonacci generates correct sequence

---

Next: **Summary** - recap Functions!
