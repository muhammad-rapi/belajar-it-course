## Lambda Functions

**Lambda** = anonymous function (function tanpa nama). One-liner.

---

### Syntax

```python
lambda arguments: expression
```

**Contoh**:

```python
# Regular function
def tambah(a, b):
    return a + b

# Lambda equivalent
tambah = lambda a, b: a + b

print(tambah(5, 3))  # 8
```

---

### Use Case: Inline Function

**Sort by custom key**:

```python
users = [
    {"name": "Rafi", "age": 25},
    {"name": "Budi", "age": 30},
    {"name": "Siti", "age": 22}
]

# Sort by age
sorted_users = sorted(users, key=lambda u: u["age"])
print(sorted_users)
# [{'name': 'Siti', 'age': 22}, {'name': 'Rafi', 'age': 25}, ...]
```

**Filter**:

```python
numbers = [1, 2, 3, 4, 5, 6]
even = list(filter(lambda x: x % 2 == 0, numbers))
print(even)  # [2, 4, 6]
```

**Map**:

```python
numbers = [1, 2, 3, 4, 5]
squared = list(map(lambda x: x**2, numbers))
print(squared)  # [1, 4, 9, 16, 25]
```

---

### Lambda vs Regular Function

**Lambda**:
- One-liner
- Inline use
- No name

**Regular function**:
- Multi-line
- Reusable
- Named

**When to use lambda**: Simple operations (sort key, filter, map).  
**When to use regular**: Complex logic, reusability.

---

Next: **Exercises** - praktek functions!
