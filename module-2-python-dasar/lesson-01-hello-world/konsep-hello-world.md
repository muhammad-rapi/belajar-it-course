## Hello World - Program Pertama

"Hello World" itu tradisi programmer. Program pertama selalu print "Hello, World!" buat pastiin setup lu bener.

### Step 1: Bikin File Python

1. Buka VS Code
2. Bikin folder baru: `belajar-python`
3. Di dalam folder itu, bikin file: `hello.py`

> **Note**: Extension `.py` = file Python. Komputer tau ini code Python, bukan text biasa.

### Step 2: Tulis Code

Ketik ini di `hello.py`:

```python
print("Hello, World!")
```

Itu doang. Satu baris.

### Step 3: Jalankan

**Cara 1: Lewat Terminal**
1. Buka Terminal di VS Code (shortcut: Ctrl+` atau Cmd+`)
2. Pastiin lu ada di folder `belajar-python`
3. Ketik: `python3 hello.py`
4. Enter

**Cara 2: Lewat VS Code Run Button**
1. Klik kanan di editor → pilih "Run Python File in Terminal"

**Output yang keluar**:
```
Hello, World!
```

Kalau keluar itu, **selamat, lu udah jadi programmer** 🎉

---

## Apa yang Terjadi?

Mari kita bedah:

```python
print("Hello, World!")
```

- **`print`** = fungsi built-in Python buat nampilin output ke layar
- **`( )`** = tanda kurung, tempat lu kasih input ke fungsi
- **`"Hello, World!"`** = string (text) yang mau ditampilin
- **`;`** = NGGAK PERLU di Python (ini bukan JavaScript/C++)

**Bayangin `print()` kayak pengeras suara di stasiun**: Lu kasih pesan, pengeras suara ngumumin. Bedanya, `print()` "ngumumin" ke Terminal.

---

## Coba Ubah

Sekarang coba ubah text-nya:

```python
print("Nama gue Rafi")
print("Gue belajar Python")
print("Ini keren banget!")
```

Run lagi. Output:
```
Nama gue Rafi
Gue belajar Python
Ini keren banget!
```

Tiap `print()` = satu baris output.

---

## Kesalahan Umum

### 1. Lupa Tanda Kutip

```python
print(Hello, World!)  # ❌ Error: NameError
```

**Kenapa error?**: Python mikir `Hello` itu nama variable (nanti kita bahas). Text harus pake kutip `"..."` atau `'...'`.

**Fix**:
```python
print("Hello, World!")  # ✅
```

### 2. Salah Ketik Nama Fungsi

```python
Print("Hello")  # ❌ Error: NameError: name 'Print' is not defined
```

**Kenapa error?**: Python **case-sensitive**. `print` ≠ `Print`. Huruf kecil semua.

**Fix**:
```python
print("Hello")  # ✅
```

### 3. Lupa Kurung

```python
print "Hello"  # ❌ SyntaxError (Python 3)
```

**Kenapa error?**: Syntax Python 3 wajib pake kurung `()`. Python 2 nggak wajib, tapi Python 2 udah deprecated.

**Fix**:
```python
print("Hello")  # ✅
```

---

## Rangkuman

- `print()` = tampilin text ke Terminal
- Text harus pake kutip `"..."` (string)
- Python case-sensitive: `print` ≠ `Print`
- Satu `print()` = satu baris output

Next: **Variables** - cara simpen data biar bisa dipake berulang kali.
