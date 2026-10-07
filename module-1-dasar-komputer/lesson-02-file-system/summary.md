# Ringkasan: File System & Path

## Key Takeaways

### 1. File System Hierarchy
- **Root directory**: Titik awal semua files/folders (C:/ di Windows, / di macOS/Linux)
- **Home directory**: Folder pribadi user
- **Tree structure**: Folders bisa nested (parent/child/sibling)

### 2. Paths
**Absolute path**: Alamat lengkap dari root  
**Relative path**: Alamat relatif dari current directory

**Special symbols**:
- `.` = current directory
- `..` = parent directory (naik 1 level)
- `~` = home directory

### 3. File Extensions
- Extension = 3-4 huruf setelah dot (.txt, .jpg, .exe)
- Ngasih tau OS file type apa, buka pakai app apa
- Security: Hati-hati dengan double extension (.pdf.exe)

**Common extensions**:
- Documents: .txt, .docx, .pdf, .xlsx
- Images: .jpg, .png, .gif
- Code: .py, .js, .html, .css
- Archives: .zip, .rar

### 4. Permissions
**Windows**: Attributes (Read-only, Hidden)  
**macOS/Linux**: Read (r), Write (w), Execute (x) untuk Owner/Group/Others

**Common permissions**:
- `644`: Files (owner read/write, others read-only)
- `755`: Folders & executables
- `600`: Sensitive files (owner-only)

---

## Kesalahan Umum yang Harus Dihindari

❌ **Hide Extensions**: Ga tau file asli apa, malware bisa nyamar  
✅ **Unhide extensions** di File Explorer/Finder

❌ **Duplikat Files Tanpa Struktur**: `dokumen_final_v2_REAL.docx`  
✅ **Bikin folder structure proper** atau pakai version control (Git)

❌ **chmod 777 Sembarangan**: Everyone bisa edit/delete  
✅ **Pakai permission reasonable** (644 for files, 755 for folders)

---

## Apa Selanjutnya?

Sekarang kamu udah ngerti file system. Next step: **Command Line**.

Di Lesson 3, kamu akan belajar:
- Navigate folders via Terminal/Command Prompt
- Create/delete files tanpa GUI
- Batch operations (rename 100 files sekaligus)
- Shell commands dasar

File system adalah fondasi. Command Line adalah superpowernya.

---

**Lanjut ke [Lesson 3: Command Line Basics →](../lesson-03-command-line/intro.md)**
