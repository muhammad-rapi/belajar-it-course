## Folder dan Path

### Root

**Root** adalah titik awal tertinggi di file system. Semua folder dan file ada di bawahnya.

- Windows: `C:\` (drive C)
- macOS dan Linux: `/` (satu garis miring)

```
C:\                          <- root (Windows)
├── Program Files\           <- aplikasi yang terpasang
├── Windows\                 <- file sistem OS
└── Users\                   <- folder semua pengguna
    ├── Rafi\
    ├── Budi\
    └── Public\
```

```
/                            <- root (macOS dan Linux)
├── Applications/            <- aplikasi yang terpasang (macOS)
├── System/                  <- file sistem OS (macOS)
├── Users/                   <- folder semua pengguna (macOS)
│   ├── rafi/
│   └── budi/
└── tmp/                     <- file sementara
```

Coba perhatikan: Windows pakai garis miring terbalik (`\`), macOS dan Linux pakai garis miring biasa (`/`). Nanti waktu coding, ini bisa jadi sumber error.

---

### Path Absolut

Path absolut adalah alamat **lengkap dari root**. Seperti alamat rumah dari nama negara sampai nomor unit.

```
C:\Users\Rafi\Documents\Kerja\Laporan.docx          (Windows)
/Users/rafi/Documents/Kerja/Laporan.docx               (macOS)
```

Path absolut selalu bisa dipakai dari mana pun, karena nggak bergantung lu lagi di folder mana.

---

### Path Relatif

Path relatif adalah alamat **dari posisi lu sekarang**. Seperti bilang ke temen yang udah di Sudirman, "Thamrin Residence jalan 500 meter dari sini". Nggak perlu nyebut Indonesia lagi.

Misalnya lu lagi ada di folder `Documents`:

```
Kerja/Laporan.docx          <- masuk ke subfolder Kerja
../Downloads/foto.jpg       <- naik satu level, lalu masuk Downloads
```

Tiga simbol yang perlu dihafal:

| Simbol | Artinya |
|---|---|
| `.` | folder tempat lu sekarang |
| `..` | folder di atasnya (parent) |
| `~` | folder home lu (macOS dan Linux) |

Path relatif lebih pendek, tapi bergantung pada posisi. Kalau lu pindah folder, path yang sama bisa jadi nggak nemu apa-apa.

---

### Pohon Folder

Struktur folder sering disebut **pohon** karena bercabang:

```
Rafi\
├── Documents\
│   ├── Kerja\
│   │   ├── Laporan.docx
│   │   └── Data.xlsx
│   └── Pribadi\
│       └── Catatan.txt
├── Downloads\
│   ├── installer.exe
│   └── foto-liburan.jpg
└── Pictures\
    └── Keluarga\
        └── IMG_001.jpg
```

Istilah yang dipakai:

- **Parent**: folder di atas. `Documents` adalah parent dari `Kerja`.
- **Child**: folder di bawah. `Kerja` adalah child dari `Documents`.
- **Sibling**: folder yang sejajar. `Kerja` dan `Pribadi` itu sibling.

---

### Folder Home

**Home** adalah folder pribadi lu. Dokumen, download, dan foto lu ada di sini.

| Sistem | Lokasi home |
|---|---|
| Windows | `C:\Users\namalu\` |
| macOS | `/Users/namalu/` |
| Linux | `/home/namalu/` |

Di terminal macOS dan Linux, `~` adalah jalan pintas ke home:

```bash
cd ~              # pindah ke home
cd ~/Documents    # langsung ke Documents tanpa nulis path lengkap
```

---

### Folder Sistem yang Jangan Diutak-atik

**Windows**

- `Program Files` dan `Program Files (x86)`: aplikasi yang terpasang
- `Windows`: file inti sistem operasi. Jangan hapus atau ubah isinya.

**macOS**

- `Applications`: aplikasi yang terpasang
- `Library` dan `System`: pengaturan dan file inti. Jangan hapus atau ubah isinya kalau lu belum paham.
- `Volumes`: flash disk dan hard disk eksternal yang tersambung

Menghapus file di folder-folder ini bisa bikin sistem nggak bisa nyala.

---

### File Tersembunyi

Di macOS dan Linux, file atau folder yang namanya diawali titik (`.`) disembunyikan. Di Windows, ada atribut "Hidden". Contohnya:

```
.git/        <- riwayat Git (hidden)
.env         <- biasanya berisi password dan API key
```

Lu bakal sering ketemu ini waktu coding. Cara melihatnya:

- Windows: File Explorer, tab View, centang **Hidden items**
- macOS: di Finder, tekan `Cmd + Shift + .`
- Terminal: `ls -a` (macOS dan Linux) atau `dir /a` (Windows CMD)
