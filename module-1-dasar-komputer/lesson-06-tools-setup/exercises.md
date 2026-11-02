## Exercises

### Latihan 1: Cek Semua Instalasi

Buka terminal baru dan jalankan:

```bash
code --version
python3 --version
git --version
node --version
npm --version
```

Di Windows, ganti `python3` dengan `python`.

Salin hasilnya ke catatan lu. Kalau ada yang error, buka bagian Kesalahan Umum.

Kalau `code --version` nggak dikenali di Mac, buka VS Code, tekan `Cmd + Shift + P`, ketik "shell command", lalu pilih **Install 'code' command in PATH**.

---

### Latihan 2: Program Python Pertama

1. Bikin folder `latihan-setup` di tempat yang gampang lu cari, misalnya Documents.
2. Buka folder itu di VS Code (File, lalu Open Folder).
3. Bikin file `kenalan.py` dengan isi:

```python
nama = "Isi dengan nama lu"
print("Halo, nama aku", nama)
```

4. Jalankan lewat tombol segitiga, atau dari terminal VS Code:

```bash
python3 kenalan.py
```

**Hasil yang benar**: tulisan `Halo, nama aku` diikuti nama lu muncul di terminal.

---

### Latihan 3: Halaman HTML dengan Live Server

1. Di folder yang sama, bikin file `index.html`:

```html
<!DOCTYPE html>
<html>
  <body>
    <h1>Halaman Pertama</h1>
    <p>Dibuat dengan VS Code.</p>
  </body>
</html>
```

2. Klik kanan di file itu, pilih **Open with Live Server**.
3. Browser terbuka. Sekarang ganti teks di `<h1>`, simpan, dan liat browser berubah sendiri.
4. Buka DevTools di halaman itu (materi Lesson 5) dan cari tag `<h1>` di tab Elements.

---

### Latihan 4: Git Config

Jalankan:

```bash
git config --global user.name
git config --global user.email
```

**Hasil yang benar**: nama dan email yang tadi lu atur muncul. Kalau kosong, ulangi perintah `git config --global` dari materi Install Git.

---

### Latihan 5: JavaScript dengan Node.js

Bikin `hitung.js`:

```javascript
const harga = 15000;
const jumlah = 3;
console.log("Total:", harga * jumlah);
```

Jalankan `node hitung.js`.

**Hasil yang benar**: `Total: 45000`.

Lalu ubah angkanya, jalankan lagi, dan pastikan hasilnya ikut berubah.
