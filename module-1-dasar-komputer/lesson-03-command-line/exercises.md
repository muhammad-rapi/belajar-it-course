## Exercises - Command Line Basics

Praktek langsung di terminal. **Ketik manual**, jangan copy-paste.

---

### Exercise 1: Basic Navigation

**Tujuan**: Navigasi folder dan cek posisi.

**Yang Perlu Lu Lakukan**:
1. Buka terminal
2. Cek posisi sekarang (`pwd`)
3. Balik ke home (`cd ~`)
4. Pindah ke Desktop
5. Liat isi Desktop
6. Balik ke home lagi

**Commands**:
```bash
pwd
cd ~
cd Desktop
ls
cd ~
pwd
```

**Expected**: Tiap command jalan tanpa error, lu bisa lihat isi Desktop.

---

### Exercise 2: Bikin Project Folder

**Tujuan**: Bikin struktur folder project.

**Yang Perlu Lu Lakukan**:

Bikin struktur ini:
```
belajar-python/
├── src/
├── tests/
└── docs/
```

**Commands**:
```bash
cd ~/Desktop
mkdir belajar-python
cd belajar-python
mkdir src tests docs
ls
```

**Expected Output** (dari `ls`):
```
docs  src  tests
```

---

### Exercise 3: Bikin File

**Tujuan**: Bikin file di folder project.

**Lanjutan dari Exercise 2:**

```bash
cd src
touch main.py
touch utils.py
ls
```

**Expected**:
```
main.py  utils.py
```

---

### Exercise 4: Copy & Move

**Tujuan**: Copy file dan pindah folder.

**Yang Perlu Lu Lakukan**:
1. Copy `main.py` jadi `backup.py`
2. Pindah `backup.py` ke folder `tests`
3. Cek isi folder `tests`

**Commands**:
```bash
# Masih di folder src
cp main.py backup.py
ls               # Harusnya ada backup.py

mv backup.py ../tests/
ls               # backup.py udah ga ada

cd ../tests
ls               # backup.py ada di sini
```

---

### Exercise 5: Navigation Challenge

**Tujuan**: Navigasi pakai relative path.

**Starting point**: Lu di `/Desktop/belajar-python/tests`

**Task**: Pindah ke `src` folder pakai relative path.

**Commands**:
```bash
pwd              # .../belajar-python/tests
cd ../src        # Naik 1 level, masuk src
pwd              # .../belajar-python/src
```

**Bonus**: Dari `src`, pindah ke `docs` pakai 1 command.

```bash
cd ../docs
```

---

### Exercise 6: Cleanup

**Tujuan**: Hapus project folder.

**Yang Perlu Lu Lakukan**:
1. Balik ke Desktop
2. Hapus folder `belajar-python` beserta isinya

**Commands**:
```bash
cd ~/Desktop
rm -r belajar-python
ls               # belajar-python harusnya udah ga ada
```

---

## Checklist

Abis ngerjain semua:
- [ ] Lu bisa buka terminal tanpa bingung
- [ ] Lu paham `pwd`, `cd`, `ls`, `mkdir`, `touch`, `rm`, `cp`, `mv`
- [ ] Lu bisa navigasi folder pakai relative path (`..`, `.`)
- [ ] Lu ga takut lagi sama terminal

---

## Troubleshooting

**Command not found**:
```bash
cdd Desktop  # Typo, harusnya 'cd'
# bash: cdd: command not found
```
→ Cek spelling, pake Tab autocomplete.

**No such file or directory**:
```bash
cd Dokumen  # Typo, harusnya 'Documents'
# cd: no such file or directory: Dokumen
```
→ Cek nama folder pake `ls`, case-sensitive di macOS/Linux.

**Permission denied**:
```bash
rm /System/file.txt
# rm: cannot remove '/System/file.txt': Permission denied
```
→ Beberapa folder system-protected. Ga usah dipaksa.

---

Next: **Summary** - ringkasan command line basics.
