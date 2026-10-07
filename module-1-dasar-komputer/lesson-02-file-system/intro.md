# File System & Path

## Kenapa Perlu Belajar Ini?

Bayangin kamu punya rumah dengan 1000 barang. Baju, buku, alat masak, mainan anak, dokumen penting — semua campur aduk di satu kamar. Mau cari apa-apa susah. Mau ngerapiin? Lebih susah lagi.

Komputer kamu juga begitu. Ada ribuan file: foto keluarga, dokumen kerja, installer aplikasi, video YouTube yang di-download, screenshot random — semua nyampur. Bedanya, komputer punya sistem buat ngatur ini semua: **file system**.

**Tanpa ngerti file system, kamu akan**:
- Bingung nyari file (download dimana ya?)
- Duplikat file berulang kali (dokumen_final.docx, dokumen_final_v2.docx, dokumen_final_FINAL.docx)
- Kehabisan space karena ga tau file besar ada dimana
- Susah collab (kalo kerja bareng, gimana share struktur folder yang sama?)
- Susah coding (programmer HARUS paham path untuk akses file)

## Apa yang Akan Kamu Pelajari

Setelah lesson ini, kamu bisa:
- Ngerti struktur folder komputer (dari root sampai file individual)
- Bedain absolute path vs relative path
- Tau file types (extension) dan kegunaannya
- Paham konsep permissions (siapa boleh baca/edit file)
- Navigasi file system dengan percaya diri

**Durasi**: ~20 menit baca + 30 menit praktek

---

## Analogi: File System = Sistem Alamat Rumah

> Kamu mau kirim paket ke temen di Jakarta. Ga cukup bilang "rumah si Budi". Kamu butuh alamat lengkap:
> 
> **Indonesia** → **DKI Jakarta** → **Jakarta Selatan** → **Jl. Sudirman No. 123** → **Apartemen Thamrin** → **Lantai 15** → **Unit 1505**

Komputer works exactly like this:

```
C:\                           ← Root (negara)
└── Users\                    ← Folder users (provinsi)
    └── Rafi\                 ← User kamu (kota)
        └── Documents\        ← Folder Documents (jalan)
            └── Kerja\        ← Subfolder Kerja (gedung)
                └── Laporan.docx  ← File (unit rumah)
```

Ini yang disebut **path** (alamat file).

---

## Kenapa Path Penting Banget?

**Skenario 1: Kamu belajar coding**
```python
# Kamu mau buka file data.csv
file = open("data.csv")  # ERROR: File not found
```

Kenapa error? Karena Python cari di **current directory** (folder dimana kamu run script). Kalo `data.csv` ada di folder lain, Python ga tau.

Solution:
```python
# Kasih full path
file = open("C:/Users/Rafi/Documents/Kerja/data.csv")  # Works!
```

**Skenario 2: Kamu install software**
Software tanya: "Install dimana?" Default biasanya `C:\Program Files\`. Kalo kamu ga ngerti, nanti susah uninstall atau cari file config-nya.

**Skenario 3: Command Line**
```bash
cd /Users/Rafi/Projects  # Pindah ke folder Projects
python script.py         # Run script di folder itu
```

Tanpa ngerti path, kamu ga bisa navigasi command line.

---

## Struktur Lesson Ini

Kita akan bahas step-by-step:
1. **File System Hierarchy** — struktur folder (root, subfolder, file)
2. **File Types** — extension (.txt, .jpg, .exe) dan kegunaannya
3. **Permissions** — siapa boleh baca/edit/hapus file
4. **Hands-on Exercises** — eksplorasi file system kamu sendiri

Mari kita mulai! 🚀
