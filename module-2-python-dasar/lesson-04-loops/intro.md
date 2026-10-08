## Kenapa Perlu Loops?

Lu perlu cetak 1-100. Cara manual:

```python
print(1)
print(2)
print(3)
# ... copas 97x lagi
print(100)
```

**100 baris code buat hal sepele**. Kalau ada typo? Edit 100 tempat.

---

### Solusi: Loop

```python
for i in range(1, 101):
    print(i)
```

**3 baris**. Beres.

---

### Contoh Real

**Kirim email ke 1000 customer**:

Tanpa loop (impossible):
```python
send_email("customer1@mail.com")
send_email("customer2@mail.com")
# ... 998x lagi???
```

Dengan loop:
```python
customers = get_all_customers()  # 1000 data

for customer in customers:
    send_email(customer.email)
```

**4 baris, handle 1000 email**.

---

### Loop Ada Dimana-Mana

- Instagram feed → loop posts
- Spotify playlist → loop songs
- E-commerce → loop products
- Chat app → loop messages

Semua app pake loop.

---

## Apa yang Lu Bakal Pelajari

- **For loop**: iterate list/range
- **While loop**: loop dengan kondisi
- **Loop control**: break, continue, pass
- **Nested loops**: loop dalam loop

Ready? Let's loop! 🔁
