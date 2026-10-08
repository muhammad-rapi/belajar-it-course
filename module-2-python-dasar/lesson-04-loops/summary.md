## Summary - Loops

Lu udah bisa otomatin repetitive tasks dengan loops.

---

## Key Concepts

### For Loop
```python
for item in collection:
    # iterate list, range, string, dict
```

**Use case**: Lu tau berapa kali loop (iterate list, range).

### While Loop
```python
while kondisi:
    # loop sampe kondisi False
```

**Use case**: Lu ga tau berapa kali loop (validasi input, menu).

### Loop Control

| Keyword | Fungsi |
|---------|--------|
| `break` | Stop loop |
| `continue` | Skip ke next iteration |
| `pass` | Placeholder (do nothing) |

### Nested Loops
```python
for i in outer:
    for j in inner:
        # loop dalam loop
```

**Warning**: Performance O(n²) atau lebih. Hindari kalau bisa.

---

## Common Patterns

**Sum list**:
```python
total = sum(numbers)  # built-in
# atau manual:
total = 0
for num in numbers:
    total += num
```

**Filter list**:
```python
even = [x for x in numbers if x % 2 == 0]  # list comprehension
# atau manual:
even = []
for x in numbers:
    if x % 2 == 0:
        even.append(x)
```

**Find item**:
```python
for item in items:
    if item == target:
        print("Found!")
        break
```

---

## Tips

**1. Pilih loop yang tepat**
- Iterate collection → for
- Loop sampe kondisi → while

**2. Avoid infinite loop**
```python
while True:
    # Pastikan ada break atau kondisi jadi False
```

**3. Use built-in functions**
```python
# ✅ Better
total = sum(numbers)
max_val = max(numbers)

# ❌ Manual loop (lebih lambat)
total = 0
for num in numbers:
    total += num
```

**4. List comprehension** (next level)
```python
# ✅ Compact
squared = [x**2 for x in range(10)]

# ❌ Verbose
squared = []
for x in range(10):
    squared.append(x**2)
```

---

## Next Steps

**Next lesson: Functions** - organize code jadi reusable blocks.

Preview:
- Define function
- Parameters & arguments
- Return values
- Scope
- Lambda functions

Sebelum lanjut:
- [ ] Paham for vs while
- [ ] Bisa pake break/continue
- [ ] Comfortable dengan nested loops
- [ ] FizzBuzz solved

---

Ready buat Functions! 🚀
