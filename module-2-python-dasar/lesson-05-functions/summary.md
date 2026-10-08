## Summary - Functions

Lu udah bisa organize code jadi reusable blocks.

---

## Key Concepts

### Define Function
```python
def nama_func(param1, param2=default):
    # code
    return result
```

### Scope
- **Local**: Variable di dalam function
- **Global**: Variable di luar function
- Hindari modify global, pass parameter instead

### *args & **kwargs
```python
def func(*args, **kwargs):
    # args = tuple
    # kwargs = dict
```

### Lambda
```python
lambda a, b: a + b
```

One-liner, anonymous function.

---

## Best Practices

**1. Descriptive names**
```python
# ✅ Good
def hitung_total_harga(items):
    pass

# ❌ Bad
def calc(x):
    pass
```

**2. Single responsibility**
```python
# ✅ Good
def validate_email(email):
    pass

def send_email(to, subject, body):
    pass

# ❌ Bad
def validate_and_send_email(email, subject, body):
    pass  # too many responsibilities
```

**3. Use docstrings**
```python
def tambah(a, b):
    """Tambahkan 2 angka."""
    return a + b
```

**4. Default parameters di akhir**
```python
# ✅ Good
def func(a, b, c=10):
    pass

# ❌ Bad
def func(a, b=10, c):
    pass
```

**5. Return early**
```python
# ✅ Good
def divide(a, b):
    if b == 0:
        return "Error"
    return a / b

# ❌ Bad (nested)
def divide(a, b):
    if b != 0:
        return a / b
    else:
        return "Error"
```

---

## Common Mistakes

**1. Forget return**
```python
def tambah(a, b):
    a + b  # ❌ ga return

result = tambah(5, 3)
print(result)  # None
```

**2. Modify mutable default parameter**
```python
# ❌ Bug
def add_item(item, items=[]):
    items.append(item)
    return items

# ✅ Fix
def add_item(item, items=None):
    if items is None:
        items = []
    items.append(item)
    return items
```

---

## Next Steps

**Next lesson: Project - Automation Script** - apply semua yang udah dipelajari!

Preview:
- File automation
- Web scraping
- Data processing
- CLI tool

Sebelum lanjut:
- [ ] Bisa define function dengan parameters
- [ ] Paham scope (local vs global)
- [ ] Comfortable dengan *args/**kwargs
- [ ] Calculator & grade calculator works

---

Ready buat final project! 🚀
