# Praktek: File System & Path

## Latihan 1: Eksplorasi File System

**Tujuan**: Familiar dengan struktur folder komputer kamu.

### Yang Perlu Kamu Lakukan:

1. Buka File Explorer (Windows) atau Finder (macOS)
2. Navigate ke root directory (C:/ atau /)
3. Explore folders: Program Files / Applications, Users
4. Masuk ke home directory kamu
5. Document path dari Downloads folder

**Expected**: Kamu bisa tau absolute path dari folder-folder penting.

---

## Latihan 2: Absolute vs Relative Path

**Tujuan**: Praktek bedain absolute dan relative path.

### Setup:
Bikin struktur folder di Desktop:
```
MyProject/
├── src/
│   └── main.py
└── data/
    └── input.csv
```

### Task:
1. Tulis absolute path untuk `main.py` dan `input.csv`
2. Dari folder `src/`, tulis relative path ke `input.csv`

<details>
<summary>Hints</summary>

- Absolute: mulai dari root
- Relative dari src/: `../data/input.csv` (naik 1 level, masuk data)
</details>

---

## Latihan 3: File Extensions

**Tujuan**: Familiar dengan common file types.

### Task:
1. Unhide extensions di File Explorer/Finder
2. Explore Downloads folder
3. Categorize 10 files berdasarkan extension (Documents, Images, Archives, etc.)

---

## Latihan 4: Permissions (macOS/Linux)

**Tujuan**: Praktek lihat dan ubah permissions.

### Task:
```bash
cd ~/Desktop
echo "Hello" > test.txt
ls -l test.txt         # Lihat permissions

chmod 444 test.txt     # Make read-only
echo "Test" >> test.txt  # Should fail

chmod 644 test.txt     # Restore write
echo "Test" >> test.txt  # Works
```

---

## Challenge: Build Project Structure

Bikin struktur web project:
```
my-website/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── script.js
└── images/
    └── logo.png
```

<details>
<summary>Solution (macOS/Linux)</summary>

```bash
mkdir -p ~/Desktop/my-website/{css,js,images}
cd ~/Desktop/my-website
touch index.html css/style.css js/script.js images/logo.png
chmod 644 *.html css/* js/* images/*
chmod 755 css js images
```
</details>

---

Lanjut ke [Summary →](./summary.md)
