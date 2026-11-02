## Install Python

Python adalah bahasa pemrograman yang dipakai di Module 2. Komputer lu nggak otomatis bisa ngejalanin file Python, jadi interpreter-nya perlu dipasang dulu.

Interpreter itu program yang baca kode Python baris demi baris dan ngejalanin perintahnya.

---

### Cek Dulu, Mungkin Udah Ada

Buka terminal dan ketik:

```bash
python3 --version
```

Kalau keluar tulisan seperti `Python 3.12.4`, lu udah punya Python 3. Pastikan angka depannya 3 dan lanjut ke bagian "Cek Hasilnya". Kalau muncul pesan error atau tawaran install, ikuti langkah di bawah.

Di Windows, perintahnya `python --version`, bukan `python3`.

---

### Langkah Install

**Windows**

1. Buka [python.org/downloads](https://www.python.org/downloads/) dan download installer versi terbaru.
2. Jalankan installer. **Di jendela pertama, centang "Add python.exe to PATH"** sebelum klik Install Now. Kalau lupa, perintah `python` nggak akan dikenali di terminal.
3. Tunggu sampai selesai, lalu klik Close.

**macOS**

1. Buka [python.org/downloads](https://www.python.org/downloads/) dan download installer macOS.
2. Buka file `.pkg` dan ikuti petunjuknya sampai selesai.

**Linux (Ubuntu / Debian)**

```bash
sudo apt update
sudo apt install python3 python3-pip python3-venv
```

---

### Cek Hasilnya

Tutup terminal lama, buka yang baru, lalu ketik:

```bash
python3 --version
```

(Windows: `python --version`)

Hasil yang benar: `Python 3.x.x`.

Kenapa terminal harus dibuka ulang? Terminal yang lagi terbuka baca daftar program waktu dia dibuka. Program yang baru dipasang baru kelihatan di terminal yang baru.

### Coba Jalanin Python

Ketik `python3` (Windows: `python`) lalu Enter. Lu masuk ke mode interaktif yang ditandai `>>>`. Coba:

```python
>>> 2 + 3
5
>>> print("Halo")
Halo
```

Keluar dengan mengetik `exit()` lalu Enter.

### Hubungkan ke VS Code

1. Buat file baru bernama `halo.py` di VS Code.
2. Isi dengan `print("Halo dari Python")`.
3. Klik ikon segitiga di pojok kanan atas editor.

Kalau tulisan "Halo dari Python" muncul di terminal bawah, VS Code dan Python udah terhubung. Kalau VS Code minta memilih interpreter, pilih versi Python 3 yang barusan lu install.
