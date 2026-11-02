## Navigasi dan Path

Path adalah alamat file atau folder. Ada dua jenis: absolut (dari root) dan relatif (dari posisi sekarang). Ini sama dengan yang lu pelajari di Lesson 2, sekarang dipakai lewat terminal.

---

### Absolute Path

Path **lengkap dari root**.

**macOS/Linux**:
```
/Users/rafi/Documents/project/app.py
```

Dimulai dari `/` (root).

**Windows**:
```
C:\Users\Rafi\Documents\project\app.py
```

Dimulai dari `C:\` (drive letter).

**Kapan pake?** Kalau lu mau refer ke file dari **mana aja**. Path selalu sama, ga peduli lu ada di folder mana.

**Contoh**:

```bash
# Lu ada di /Users/rafi/Desktop
# Tapi mau akses file di Documents
cat /Users/rafi/Documents/notes.txt  # Absolute path
```

---

### Relative Path

Path **dari posisi sekarang**.

**Contoh**:

```bash
pwd  # /Users/rafi
cd Documents         # Relative: pindah ke Documents dari posisi sekarang
pwd  # /Users/rafi/Documents
```

**Symbols**:
- `.` = folder sekarang
- `..` = parent folder (naik 1 level)
- `~` = home directory

**Contoh navigasi**:

```bash
pwd  # /Users/rafi/Documents/project

# Naik 1 level
cd ..
pwd  # /Users/rafi/Documents

# Naik 2 level
cd ../..
pwd  # /Users/rafi

# Ke folder sibling (folder sejajar)
cd Documents/project/../backup
pwd  # /Users/rafi/Documents/backup
```

---

### Contoh: Navigasi Praktis

**Struktur folder**:
```
/Users/rafi/
├── Documents/
│   ├── project/
│   │   ├── app.py
│   │   └── README.md
│   └── notes.txt
└── Desktop/
    └── test.txt
```

**Skenario 1**: Lu di `/Users/rafi/Documents/project`, mau ke Desktop

```bash
# Cara 1: Absolute
cd /Users/rafi/Desktop

# Cara 2: Relative (naik 2 level, masuk Desktop)
cd ../../Desktop

# Cara 3: Via home
cd ~/Desktop
```

**Skenario 2**: Lu di Desktop, mau liat notes.txt di Documents

```bash
# Absolute
cat /Users/rafi/Documents/notes.txt

# Relative
cat ../Documents/notes.txt
```

---

### Home Directory (`~`)

`~` = shortcut ke home directory lu.

**macOS/Linux**:
```bash
cd ~         # Ke /Users/rafi
cd ~/Desktop # Ke /Users/rafi/Desktop
```

**Windows** (PowerShell/Git Bash):
```bash
cd ~         # Ke C:\Users\Rafi
cd ~/Desktop # Ke C:\Users\Rafi\Desktop
```

**Super berguna** buat cepet balik ke home.

---

### Slash: `/` vs `\`

**macOS/Linux**: Pake `/`
```
/Users/rafi/Documents
```

**Windows**: Pake `\` (backslash)
```
C:\Users\Rafi\Documents
```

Tapi **PowerShell dan Git Bash** support `/` juga:
```bash
cd C:/Users/Rafi/Documents  # Jalan di PowerShell/Git Bash
```

**Tip**: Kalau nulis script Python/code yang cross-platform, pake `/`. Python otomatis convert ke `\` di Windows.

---

### Wildcard (Bonus)

`*` = match semua.

```bash
# List semua file .txt
ls *.txt

# Hapus semua file .log
rm *.log

# Copy semua .py ke backup
cp *.py backup/
```

**Hati-hati**: `rm *` hapus **semua file** di folder. Ga ada undo.

---

## Latihan Cepat

Coba sequence ini (jangan copy-paste, ketik manual):

```bash
pwd                      # Liat posisi sekarang
cd ~                     # Balik ke home
mkdir test-terminal      # Bikin folder
cd test-terminal
mkdir folder1 folder2    # Bikin 2 folder
touch file1.txt file2.txt
ls                       # Liat isi
cd folder1
pwd                      # /Users/rafi/test-terminal/folder1
cd ..                    # Balik ke test-terminal
cd ../..                 # Naik 2 level (ke home)
pwd                      # /Users/rafi
rm -r test-terminal      # Hapus folder test (cleanup)
```

Kalau semua jalan, navigasi dasar sudah lu kuasai.

---

Berikutnya: latihan lengkap di Exercises.
