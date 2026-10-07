# File Types & Extensions

## Apa itu Extension?

**Extension** = 3-4 huruf setelah dot (.) di nama file. Ini ngasih tau komputer "file ini tipe apa, buka pakai aplikasi apa".

**Contoh**:
- `Laporan.docx` → .docx = Microsoft Word document
- `foto.jpg` → .jpg = Image (JPEG format)
- `script.py` → .py = Python code
- `installer.exe` → .exe = Executable (program)

**Analogi**: Extension kayak label di kotak. Kamu liat "Buku Pelajaran" vs "Mainan" — langsung tau isinya apa tanpa buka.

---

## Common File Types

### Documents
| Extension | Type | Opens With |
|-----------|------|------------|
| .txt | Plain text | Notepad, TextEdit |
| .docx | Word document | Microsoft Word, Google Docs |
| .pdf | PDF document | Adobe Reader, Preview |
| .xlsx | Excel spreadsheet | Excel, Google Sheets |
| .pptx | PowerPoint | PowerPoint, Google Slides |

### Images
| Extension | Type | Use Case |
|-----------|------|----------|
| .jpg / .jpeg | Photo (compressed) | Foto kamera, web images |
| .png | Image (lossless) | Screenshots, graphics with transparency |
| .gif | Animated image | Memes, simple animations |
| .svg | Vector graphic | Logos, icons (scalable) |

### Code / Development
| Extension | Language | Description |
|-----------|----------|-------------|
| .py | Python | Python script |
| .js | JavaScript | JavaScript code |
| .html | HTML | Web page structure |
| .css | CSS | Web page styling |
| .json | JSON | Data format (config, API response) |

### Archives
| Extension | Type | Platform |
|-----------|------|----------|
| .zip | Compressed folder | Cross-platform |
| .rar | Compressed (RAR) | Needs WinRAR/7-Zip |
| .tar.gz | Compressed (Linux) | Linux/macOS |

---

## Kenapa Extension Penting?

### 1. OS Tau Aplikasi Apa yang Dipakai
Kalo kamu double-click `foto.jpg`, OS otomatis buka pakai Photos app. Double-click `dokumen.docx` → buka pakai Word.

Ini karena OS punya **file association**: mapping extension → default app.

### 2. Security
```
invoice.pdf.exe  ← DANGER! Ini bukan PDF, ini .exe (malware trick)
```

Hacker sering nyamar pake double extension. User kira PDF, ternyata executable.

**Rule**: Selalu cek extension sebelum buka file dari stranger.

### 3. Compatibility
Kalo kamu share file ke orang lain, extension matters:
- `.docx` → butuh Word (atau compatible editor)
- `.pdf` → universal, semua OS bisa buka

---

## Kesalahan Umum

### "File Corrupt" Setelah Rename Extension
**Masalah**: Kamu rename `.txt` jadi `.docx`, Word ga bisa buka.

**Solusi**: Jangan rename extension kecuali kamu tau format aslinya sama. Convert pakai tool yang bener.

### Hidden Extension = Security Risk
Kalo extension di-hide, kamu ga tau file asli apa. Malware sering exploit ini.

**Solusi**: Selalu unhide extension di File Explorer/Finder.

---

Lanjut ke [Permissions →](./konsep-permissions.md)
