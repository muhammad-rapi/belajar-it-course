## Kesalahan Umum

### 1. "command not found" atau "is not recognized" setelah install

Pesannya biasanya `python3: command not found` atau `'python' is not recognized as an internal or external command`.

Penyebab paling sering ada dua:

- **Terminal belum dibuka ulang.** Tutup terminal dan buka yang baru.
- **PATH belum diatur.** PATH adalah daftar folder yang dicek terminal waktu lu ngetik nama program. Di Windows, ini biasanya karena kotak "Add python.exe to PATH" nggak dicentang. Cara paling gampang: jalankan ulang installer Python, pilih Modify, lalu aktifkan opsi PATH, atau uninstall dan install ulang dengan kotak itu dicentang.

### 2. Python versi 2 yang kepanggil

Di sebagian sistem Linux lama, perintah `python` nunjuk ke Python 2 yang udah nggak dipakai. Selalu cek dengan `python3 --version` dan pakai `python3` di Mac dan Linux.

### 3. Install dari website tiruan

Cari nama tools di mesin pencari kadang menampilkan iklan website palsu di urutan teratas. Selalu pakai alamat resmi yang tertulis di materi ini: `code.visualstudio.com`, `python.org`, `git-scm.com`, dan `nodejs.org`. Cek ulang ejaan alamatnya sebelum download.

### 4. Pakai sudo atau jalankan sebagai admin buat semuanya

Waktu error muncul, kadang ada saran di internet buat nambahin `sudo` di depan perintah. Pakai itu cuma kalau materi atau dokumentasi resminya nyuruh. Menjalankan sembarang perintah sebagai admin bisa bikin file sistem berubah dan susah dibalikin.

### 5. Git: salah isi nama atau email

Kalau typo waktu ngatur `user.name` atau `user.email`, ulangi saja perintah `git config --global` dengan nilai yang benar. Nilai lama langsung tertimpa.

### 6. Tutup jendela installer saat masih jalan

Terutama di Mac saat Command Line Tools sedang diunduh, progress-nya kadang terlihat diam. Tunggu sampai selesai. Kalau udah lewat 30 menit tanpa perubahan, tutup dan ulangi dari awal.
