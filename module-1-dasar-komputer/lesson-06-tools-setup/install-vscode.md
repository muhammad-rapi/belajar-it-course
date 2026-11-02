## Install VS Code

VS Code (Visual Studio Code) adalah code editor gratis dari Microsoft. Fungsinya mirip Word, tapi buat nulis kode: ada pewarnaan teks, saran otomatis, dan terminal bawaan.

---

### Langkah Install

1. Buka [code.visualstudio.com](https://code.visualstudio.com/) dan klik tombol download sesuai sistem lu.
2. **macOS**: buka file `.zip` hasil download, lalu seret aplikasi VS Code ke folder Applications.
3. **Windows**: jalankan installer. Di langkah "Select Additional Tasks", centang **Add to PATH** dan opsi **Open with Code** supaya lu bisa buka folder dari klik kanan.
4. **Linux**: download file `.deb` (Ubuntu/Debian) atau `.rpm` (Fedora), lalu install lewat software center atau terminal.

### Cek Hasilnya

Buka VS Code. Kalau jendela dengan tulisan Welcome muncul, instalasi berhasil.

---

### Mengenal Tampilan

- **Explorer** (ikon dua kertas di kiri): daftar file dan folder
- **Editor** (area tengah): tempat nulis kode
- **Terminal** (buka dengan `` Ctrl + ` ``): terminal yang nempel di bawah editor
- **Extensions** (ikon kotak di kiri): tempat install tambahan

### Extension yang Dipasang Sekarang

Buka tab Extensions, cari nama berikut, lalu klik Install:

1. **Python** (dari Microsoft): dukungan nulis dan jalanin Python
2. **Prettier**: merapikan kode otomatis
3. **Live Server**: buka file HTML di browser dengan auto-refresh tiap file disimpan

Cukup tiga ini. Menambah banyak extension di awal malah bikin bingung dan memperlambat editor.

### Pengaturan yang Berguna

Buka Settings (`Cmd + ,` di Mac, `Ctrl + ,` di Windows / Linux), lalu cari:

- **Auto Save**: pilih `afterDelay`. File tersimpan otomatis dan lu nggak lupa menyimpan.
- **Format On Save**: centang. Prettier akan merapikan kode tiap lu simpan.
- **Font Size**: 14 sampai 16 biar nyaman di mata.

### Shortcut yang Layak Dihafal

- `Cmd + P` / `Ctrl + P`: buka file berdasarkan nama
- `Cmd + Shift + P` / `Ctrl + Shift + P`: command palette, tempat nyari semua perintah
- `Cmd + B` / `Ctrl + B`: tutup atau buka sidebar
- `Cmd + /` / `Ctrl + /`: jadikan baris terpilih sebagai komentar
