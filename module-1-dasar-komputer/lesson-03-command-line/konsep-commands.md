## Basic Commands

10 command paling sering dipake. Hafal ini, lu udah 80% siap.

---

### 1. `pwd` - Print Working Directory

Nunjukin **di mana lu sekarang**.

```bash
pwd
```

Output (macOS/Linux):
```
/Users/rafi
```

Output (Windows):
```
C:\Users\Rafi
```

**Use case**: Kalau bingung lu ada di folder mana.

---

### 2. `ls` - List

Liat **isi folder** sekarang.

```bash
ls
```

Output:
```
Desktop    Documents    Downloads    Music
```

**Dengan options**:

```bash
ls -l      # List format (detail: size, permission, date)
ls -a      # Show hidden files (yang diawali .)
ls -la     # Combine: detail + hidden
ls -lh     # Human-readable size (KB, MB, GB)
```

**Windows**: Pake `dir` (kalau CMD) atau `ls` (kalau PowerShell/Git Bash)

---

### 3. `cd` - Change Directory

**Pindah folder**.

```bash
cd Documents       # Pindah ke folder Documents
cd ..              # Naik 1 level (ke parent folder)
cd ~               # Balik ke home directory
cd /               # Ke root directory
```

**Contoh**:

```bash
pwd                # /Users/rafi
cd Documents
pwd                # /Users/rafi/Documents
cd ..
pwd                # /Users/rafi
```

---

### 4. `mkdir` - Make Directory

**Bikin folder** baru.

```bash
mkdir project           # Bikin 1 folder
mkdir folder1 folder2   # Bikin multiple folders
mkdir -p path/to/deep/folder  # Bikin nested folders sekaligus
```

**Contoh**:

```bash
cd Desktop
mkdir belajar-python
cd belajar-python
pwd  # /Users/rafi/Desktop/belajar-python
```

---

### 5. `touch` - Create File

**Bikin file** kosong (macOS/Linux/Git Bash).

```bash
touch hello.py        # Bikin file hello.py
touch file1.txt file2.txt  # Bikin multiple files
```

**Windows CMD**: Pake `echo. > file.txt` atau `copy nul file.txt`

---

### 6. `rm` - Remove

**Hapus file/folder**.

```bash
rm file.txt          # Hapus file
rm -r folder         # Hapus folder + isinya (recursive)
rm -rf folder        # Force delete (no confirmation)
```

**⚠️ HATI-HATI**: `rm` ga ada undo. File langsung hilang (ga ke Recycle Bin).

**Windows**: Pake `del file.txt` (file) atau `rmdir /s folder` (folder)

---

### 7. `cp` - Copy

**Copy file/folder**.

```bash
cp file.txt backup.txt           # Copy file
cp file.txt /path/to/destination # Copy ke folder lain
cp -r folder folder_backup       # Copy folder + isinya
```

**Windows**: Pake `copy` (file) atau `xcopy` (folder)

---

### 8. `mv` - Move

**Pindah atau rename** file/folder.

```bash
mv file.txt newname.txt         # Rename
mv file.txt /path/to/folder/    # Pindah ke folder lain
mv folder /new/location/        # Pindah folder
```

**Windows**: Pake `move`

---

### 9. `cat` - Concatenate

**Liat isi file** (macOS/Linux/Git Bash).

```bash
cat file.txt  # Print isi file ke terminal
```

**Windows**: Pake `type file.txt`

---

### 10. `clear` - Clear Screen

**Bersihkan terminal**.

```bash
clear
```

**Windows CMD**: Pake `cls`

**Shortcut**: `Ctrl + L` (Mac/Linux/Git Bash)

---

## Cheat Sheet

| Task | macOS/Linux | Windows CMD | PowerShell/Git Bash |
|------|-------------|-------------|---------------------|
| Liat folder sekarang | `pwd` | `cd` | `pwd` |
| Liat isi folder | `ls` | `dir` | `ls` |
| Pindah folder | `cd folder` | `cd folder` | `cd folder` |
| Bikin folder | `mkdir folder` | `mkdir folder` | `mkdir folder` |
| Bikin file | `touch file.txt` | `echo. > file.txt` | `touch file.txt` |
| Hapus file | `rm file.txt` | `del file.txt` | `rm file.txt` |
| Hapus folder | `rm -r folder` | `rmdir /s folder` | `rm -r folder` |
| Copy file | `cp a.txt b.txt` | `copy a.txt b.txt` | `cp a.txt b.txt` |
| Pindah file | `mv a.txt b.txt` | `move a.txt b.txt` | `mv a.txt b.txt` |
| Liat isi file | `cat file.txt` | `type file.txt` | `cat file.txt` |
| Clear screen | `clear` | `cls` | `clear` |

---

## Tips Praktis

**1. Tab autocomplete**

Ketik sebagian nama folder, terus Tab:

```bash
cd Doc<Tab>  # Auto-jadi: cd Documents
```

**2. Command history**

Pencet `↑` buat liat command sebelumnya. Ga usah ketik ulang.

**3. Copy-paste di terminal**

- macOS: `Cmd + C` / `Cmd + V`
- Windows: Klik kanan → paste (atau `Ctrl + Shift + V`)
- Linux: `Ctrl + Shift + C` / `Ctrl + Shift + V`

---

Next: **Navigation** - absolute vs relative path.
