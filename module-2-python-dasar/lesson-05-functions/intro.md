## Kenapa Perlu Functions?

**Problem**: Code copas berulang-ulang.

```python
# Hitung luas persegi
panjang1 = 10
lebar1 = 5
luas1 = panjang1 * lebar1
print(f"Luas: {luas1}")

# Copas 10x buat 10 persegi? 🤮
panjang2 = 8
lebar2 = 6
luas2 = panjang2 * lebar2
print(f"Luas: {luas2}")
```

**Solusi**: Function.

```python
def hitung_luas(panjang, lebar):
    return panjang * lebar

print(hitung_luas(10, 5))  # 50
print(hitung_luas(8, 6))   # 48
```

**1 function, reuse unlimited**. Kalau ada bug, fix di 1 tempat.

---

Functions = **building blocks** program. Semua app dibangun dari functions.
