## Install Node.js

Node.js memungkinkan kode JavaScript jalan di luar browser. Selama ini JavaScript cuma hidup di dalam browser. Dengan Node.js, lu bisa ngejalanin JavaScript langsung dari terminal, dan banyak tools web modern dibangun di atasnya.

Bareng Node.js ikut terpasang **npm** (Node Package Manager), tempat lu download library JavaScript buatan orang lain. Analogi: npm itu toko aplikasi, tapi buat potongan kode.

---

### Langkah Install

1. Buka [nodejs.org](https://nodejs.org/).
2. Download versi **LTS** (Long Term Support). Versi ini yang paling stabil dan paling aman dipakai buat belajar.
3. **macOS dan Windows**: jalankan installer dan ikuti petunjuknya dengan pilihan default.
4. **Linux**: ikuti panduan resmi di halaman download Node.js sesuai distro lu, karena langkahnya berubah dari waktu ke waktu.

---

### Cek Hasilnya

Buka terminal baru, lalu ketik:

```bash
node --version
npm --version
```

Hasil yang benar: dua angka versi, misalnya `v22.x.x` dan `10.x.x`. Angka persisnya bisa beda, yang penting keduanya muncul.

### Coba Jalanin JavaScript

Buat file `halo.js` dengan isi:

```javascript
console.log("Halo dari Node.js");
```

Lalu di terminal, masuk ke folder tempat file itu disimpan dan jalankan:

```bash
node halo.js
```

Tulisan "Halo dari Node.js" harus muncul di terminal.

### Yang Perlu Lu Tau Soal npm

Untuk sekarang cukup kenal dua perintah:

```bash
npm init -y          # bikin file package.json di folder ini
npm install nama-library   # download library ke folder proyek
```

Nggak perlu dicoba sekarang. Lu bakal sering pakai ini begitu mulai bikin website.
