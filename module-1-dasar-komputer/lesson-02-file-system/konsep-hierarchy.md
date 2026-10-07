# File System Hierarchy

## Root Directory

**Root** = titik awal tertinggi di file system. Semua folder dan file ada di bawah root.

**Windows**: `C:\` (C drive)  
**macOS/Linux**: `/` (forward slash)

Bayangin ini kayak "Indonesia" di alamat. Semua provinsi/kota ada di bawahnya.

```
C:\                          ← ROOT (Windows)
├── Program Files\           ← Folder program installed
├── Windows\                 ← System files OS
└── Users\                   ← Folder semua user
    ├── Rafi\
    ├── Budi\
    └── Public\
```

```
/                            ← ROOT (macOS/Linux)
├── Applications/            ← Apps installed
├── System/                  ← OS files
├── Users/                   ← User home folders
│   ├── rafi/
│   └── budi/
└── tmp/                     ← Temporary files
```

**Coba perhatikan**:
- Windows pakai backslash `\`
- macOS/Linux pakai forward slash `/`
- Ini penting banget kalo kamu coding (harus pakai yang sesuai OS)

---

## Absolute Path vs Relative Path

### Absolute Path
**Definisi**: Alamat LENGKAP dari root.

**Analogi**: Alamat rumah lengkap (Negara → Provinsi → Kota → Jalan → Nomor)

**Contoh Windows**:
```
C:\Users\Rafi\Documents\Kerja\Laporan.docx
```

**Contoh macOS**:
```
/Users/rafi/Documents/Kerja/Laporan.docx
```

**Kegunaan**: Kalo kamu mau akses file dari MANAPUN, pakai absolute path. Pasti ketemu.

---

### Relative Path
**Definisi**: Alamat RELATIF dari posisi sekarang.

**Analogi**: Kamu lagi di Sudirman. Temen bilang "ke Thamrin residence aja, jalannya cuma 500 meter dari sini". Ga perlu sebut dari Indonesia.

**Contoh**:
Kamu lagi di folder `C:\Users\Rafi\Documents\`:
```
Kerja\Laporan.docx          ← Relative path (Kerja subfolder dari Documents)
..\Downloads\foto.jpg       ← .. artinya "naik 1 level ke atas"
```

**Special symbols**:
- `.` (single dot) = folder sekarang
- `..` (double dot) = folder parent (naik 1 level)
- `~` (tilde, macOS/Linux) = home directory kamu (`/Users/rafi`)

**Kegunaan**: Relative path lebih pendek, bagus kalo file struktur kamu tetap (project coding). Tapi kalo structure berubah, bisa error.

---

## Directory Tree (Pohon Folder)

Struktur folder disebut **tree** karena bentuknya kayak pohon terbalik:

```
C:\Users\Rafi\               ← Root (batang)
│
├── Documents\               ← Branch (cabang)
│   ├── Kerja\              ← Sub-branch
│   │   ├── Laporan.docx   ← Leaf (daun/file)
│   │   └── Data.xlsx
│   └── Pribadi\
│       └── Catatan.txt
│
├── Downloads\
│   ├── installer.exe
│   └── foto-liburan.jpg
│
└── Pictures\
    └── Keluarga\
        └── IMG_001.jpg
```

**Terminologi**:
- **Parent directory**: Folder di atasnya (Documents adalah parent dari Kerja)
- **Child directory**: Folder di bawahnya (Kerja adalah child dari Documents)
- **Sibling directories**: Folder sejajar (Kerja dan Pribadi adalah siblings)

---

## Home Directory

**Home directory** = folder pribadi user.

**Windows**: `C:\Users\[username]\`  
**macOS**: `/Users/[username]/`  
**Linux**: `/home/[username]/`

Ini folder "rumah" kamu. Semua file pribadi (Documents, Downloads, Pictures) ada di sini.

**Shortcut**:
- Windows: `%USERPROFILE%` atau `~` (PowerShell)
- macOS/Linux: `~` (tilde)

**Contoh**:
```bash
cd ~               # Pindah ke home directory
cd ~/Documents     # Langsung ke Documents tanpa sebut full path
```

---

## Common System Folders

### Windows
```
C:\
├── Program Files\       ← Software 64-bit installed
├── Program Files (x86)\ ← Software 32-bit installed
├── Windows\             ← OS system files (JANGAN DIHAPUS!)
├── Users\               ← All user files
└── Temp\                ← Temporary files (safe to delete)
```

### macOS
```
/
├── Applications/        ← Apps installed
├── Library/             ← System + app settings
├── System/              ← macOS core files (protected)
├── Users/               ← User home folders
└── Volumes/             ← External drives (USB, etc.)
```

**⚠️ WARNING**: Jangan hapus atau edit file di `Windows\`, `System\`, atau `Library\` kecuali kamu tau persis apa yang kamu lakukan. Bisa bikin OS crash.

---

## Hidden Files

File/folder yang diawali `.` (dot) di macOS/Linux atau punya attribute "Hidden" di Windows = **hidden files**.

**Contoh**:
```
.git/          ← Git version control folder (hidden)
.env           ← Environment variables (biasanya simpen API keys)
Desktop.ini    ← Windows settings file (hidden)
```

**Kenapa dihidden?**
- System files yang user biasa ga perlu liat
- Config files yang jarang diubah
- Avoid accidental deletion

**Cara lihat**:
- **Windows**: File Explorer → View → Show hidden files
- **macOS**: Finder → Cmd + Shift + . (dot)
- **Terminal**: `ls -a` (Linux/macOS) atau `dir /a` (Windows)

---

## Praktek

Buka File Explorer (Windows) atau Finder (macOS) sekarang:

1. **Navigate ke root directory** (`C:\` atau `/`)
2. **Masuk ke home directory kamu** (`C:\Users\[nama-kamu]\` atau `/Users/[nama-kamu]`)
3. **Cari folder Downloads**. Cek path-nya (klik address bar di Windows atau klik kanan → Get Info di macOS)
4. **Coba relative path**:
   - Dari Downloads, gimana path ke Documents? (hint: `../Documents`)
   - Dari Documents/Kerja, gimana path ke Downloads? (hint: `../../Downloads`)

Lanjut ke [File Types →](./konsep-file-types.md)
