## Kenapa Perlu Belajar Ini

Bayangin lu punya rumah dan semua barangnya, dari baju, buku, alat masak, sampai dokumen penting, ditumpuk di satu kamar. Mau nyari satu barang aja susah.

Komputer lu juga isinya ribuan file: foto, dokumen, installer, video hasil download, screenshot. Bedanya, komputer punya sistem buat ngatur semuanya, namanya **file system**.

### Kalau Nggak Paham File System

- Lu bingung file hasil download ada di mana.
- File numpuk dengan nama `dokumen_final`, `dokumen_final_v2`, `dokumen_final_beneran`.
- Storage penuh dan lu nggak tahu file gede itu ada di folder mana.
- Waktu coding, program lu error "file not found" padahal filenya ada.

Yang terakhir paling sering kejadian ke pemula.

### Yang Bakal Lu Bisa

- Baca struktur folder, dari root sampai satu file
- Bedain path absolut dan path relatif
- Tahu fungsi ekstensi file dan kenapa ekstensi bisa jadi jebakan
- Paham dasar permissions: siapa boleh baca, ubah, dan jalanin file

### Analogi: Alamat Rumah

Mau kirim paket ke temen di Jakarta, nggak cukup nulis "rumah Budi". Harus lengkap:

**Indonesia, DKI Jakarta, Jakarta Selatan, Jl. Sudirman No. 123, Apartemen Thamrin, Lantai 15, Unit 1505**

Komputer nulis alamat file dengan cara yang sama:

```
C:\                              <- root (negara)
└── Users\                       <- folder users (provinsi)
    └── Rafi\                    <- folder user lu (kota)
        └── Documents\           <- folder Documents (jalan)
            └── Kerja\           <- subfolder Kerja (gedung)
                └── Laporan.docx  <- file (unit)
```

Alamat itu namanya **path**.

### Kenapa Path Sering Bikin Error

Waktu lu coding, ini bakal sering ketemu:

```python
file = open("data.csv")
# FileNotFoundError: No such file or directory: 'data.csv'
```

Python nyari `data.csv` di folder tempat program dijalankan. Kalau filenya ada di folder lain, Python nggak nemu. Solusinya ngasih alamat yang benar, dan itu isi lesson ini.

Waktu pakai terminal juga sama:

```bash
cd /Users/rafi/Projects   # pindah ke folder Projects
python3 script.py         # jalanin script di folder itu
```

Tanpa paham path, lu nggak bisa pindah-pindah folder lewat terminal.
