## *args & **kwargs

Terima **variable number of arguments**.

---

### *args (positional)

```python
def tambah(*args):
    total = sum(args)
    return total

print(tambah(1, 2))          # 3
print(tambah(1, 2, 3, 4, 5)) # 15
```

**args** = tuple of arguments.

```python
def print_all(*args):
    print(type(args))  # <class 'tuple'>
    for item in args:
        print(item)

print_all("a", "b", "c")
# a
# b
# c
```

---

### **kwargs (keyword arguments)

```python
def info(**kwargs):
    print(type(kwargs))  # <class 'dict'>
    for key, value in kwargs.items():
        print(f"{key}: {value}")

info(name="Rafi", age=25, city="Jakarta")
# name: Rafi
# age: 25
# city: Jakarta
```

---

### Kombinasi

**Order**: regular params → *args → **kwargs

```python
def func(a, b, *args, **kwargs):
    print(f"a: {a}")
    print(f"b: {b}")
    print(f"args: {args}")
    print(f"kwargs: {kwargs}")

func(1, 2, 3, 4, 5, x=10, y=20)
# a: 1
# b: 2
# args: (3, 4, 5)
# kwargs: {'x': 10, 'y': 20}
```

---

### Real Use Case: Wrapper Function

```python
def log_call(func):
    def wrapper(*args, **kwargs):
        print(f"Calling {func.__name__}")
        result = func(*args, **kwargs)
        print(f"Result: {result}")
        return result
    return wrapper

@log_call
def tambah(a, b):
    return a + b

tambah(5, 3)
# Calling tambah
# Result: 8
```

---

Next: **Lambda** - anonymous functions.
