## Cara Browser Menampilkan Halaman

Waktu lu ketik alamat website dan tekan Enter, browser ngelakuin dua tahap besar. Tahap pertama udah lu pelajari di Lesson 4: minta data ke server lewat HTTP. Tahap kedua adalah ngubah data itu jadi tampilan.

---

### Tiga Bahan Utama Sebuah Halaman

Server biasanya ngirim tiga jenis file:

**HTML** nentuin isi dan struktur. Mana judul, mana paragraf, mana gambar, mana tombol.

**CSS** nentuin tampilan. Warna, ukuran huruf, jarak, posisi.

**JavaScript** nentuin perilaku. Apa yang terjadi waktu tombol diklik, kapan data diambil dari server, kapan menu muncul.

Analogi gampangnya rumah. HTML itu kerangka dan temboknya, CSS itu cat dan dekorasinya, JavaScript itu listrik dan saklarnya.

---

### Urutan Kerja Browser

Contoh HTML sederhana:

```html
<h1>Warung Bu Sari</h1>
<p>Buka setiap hari</p>
```

Browser memprosesnya begini:

1. **Baca HTML**, lalu bikin struktur pohon yang namanya DOM (Document Object Model). Setiap tag jadi satu cabang. `<h1>` dan `<p>` jadi dua cabang di bawah `<body>`.
2. **Baca CSS**, lalu catat aturan tampilan buat tiap elemen.
3. **Gabungin keduanya** buat nentuin elemen mana yang tampil dan gayanya apa.
4. **Hitung posisi**. Elemen ini lebarnya berapa, ada di koordinat mana.
5. **Gambar ke layar**. Piksel-piksel diwarnai sesuai hasil hitungan.

Kalau ada JavaScript yang ngubah DOM, misalnya nambah satu paragraf baru, browser ngulang sebagian langkah di atas. Itu sebabnya halaman bisa berubah tanpa reload.

Coba perhatikan satu hal: DOM itu bukan file HTML-nya. DOM adalah versi hidup yang ada di memori browser. File HTML tetap sama, tapi DOM bisa berubah-ubah. Nanti di DevTools lu bakal liat DOM, bukan file aslinya.

---

### Mesin di Dalam Browser

Browser punya beberapa bagian dengan tugas berbeda:

- **Rendering engine**: ngubah HTML dan CSS jadi tampilan. Chrome dan Edge pakai Blink, Safari pakai WebKit, Firefox pakai Gecko.
- **JavaScript engine**: ngejalanin kode JavaScript. Chrome dan Edge pakai V8, Firefox pakai SpiderMonkey.
- **Networking**: ngurus request dan response HTTP.
- **Storage**: nyimpen data kecil di komputer lu, seperti cookies dan localStorage.

Lu nggak perlu hafal nama-nama ini. Yang berguna: kalau sebuah website tampil beda di Chrome dan Firefox, penyebabnya sering di perbedaan engine ini.

---

### Cookies dan localStorage

Dua-duanya tempat browser nyimpen data kecil buat sebuah website.

**Cookies** ikut terkirim ke server di setiap request. Biasanya dipakai buat nandain lu udah login.

**localStorage** cuma disimpen di browser dan nggak otomatis dikirim ke server. Cocok buat nyimpen preferensi, misalnya mode gelap.

Analoginya cookies itu kartu member yang lu tunjukin ke kasir tiap belanja. localStorage itu catatan pribadi di dompet yang cuma lu yang baca.
