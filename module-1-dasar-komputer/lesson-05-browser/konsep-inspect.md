## Inspect Element & Console

Dua fitur ini yang bakal paling sering lu pakai.

---

### Inspect Element

**Langkah**:

1. Buka halaman apa aja. Buat latihan, pakai `example.com` yang isinya sederhana.
2. Klik kanan di judul halaman, pilih **Inspect**.
3. DevTools kebuka di tab Elements, dan baris HTML judul tadi udah ke-highlight.

Di panel Elements lu bisa:

- **Ngubah teks**: klik dua kali di teks dalam tag, ketik teks baru, tekan Enter. Tampilan halaman langsung berubah.
- **Ngubah CSS**: di panel sebelah kanan (Styles) lu liat aturan CSS yang kepakai di elemen itu. Klik nilai warna, ganti, dan hasilnya langsung kelihatan.
- **Matiin aturan CSS**: ada kotak centang di sebelah tiap aturan. Hilangin centangnya buat liat tampilan tanpa aturan itu. Cara ini cepat buat nyari aturan mana yang bikin layout berantakan.
- **Hapus elemen**: pilih baris HTML, tekan `Delete`.

Ingat, semua perubahan ini cuma ada di browser lu. File asli di server nggak berubah. Refresh halaman, dan semuanya balik seperti semula.

---

### Membaca Box Model

Di Styles panel, scroll ke bawah sampai ketemu diagram kotak berlapis. Itu box model, dan setiap elemen HTML punya satu.

Dari dalam ke luar:

- **Content**: isi elemennya
- **Padding**: ruang kosong di dalam batas elemen
- **Border**: garis tepi
- **Margin**: jarak ke elemen lain

Analogi: sebuah frame foto. Foto adalah content, jarak antara foto dan bingkai adalah padding, bingkainya adalah border, dan jarak antar frame di dinding adalah margin.

Kalau jarak antar elemen kelihatan aneh, buka box model ini. Biasanya langsung ketauan kalau ada margin atau padding yang kegedean.

---

### Console

Tab Console punya dua fungsi.

**1. Nampilin pesan dari halaman**

Error JavaScript muncul di sini dengan warna merah, lengkap dengan nama file dan nomor barisnya. Contoh:

```
Uncaught TypeError: Cannot read properties of null (reading 'textContent')
    at app.js:12
```

Cara bacanya: ada kode di `app.js` baris 12 yang mencoba baca `textContent` dari sesuatu yang kosong (`null`). Biasanya karena elemen yang dicari nggak ketemu di halaman.

**2. Tempat nyoba JavaScript langsung**

Ketik ini di Console, lalu Enter:

```javascript
console.log("Halo dari Console")
```

Lalu coba yang mengubah halaman:

```javascript
document.querySelector("h1").textContent = "Judul Baru"
```

Kode itu artinya: cari elemen `h1` pertama di halaman, lalu ganti isi tulisannya. Hasilnya langsung kelihatan.

Console itu tempat coba-coba yang aman. Kalau ragu sebuah kode JavaScript bakal jalan atau nggak, tes dulu di sini.

---

### Perhatian: Jangan Tempel Kode dari Orang Asing

Console bisa ngejalanin apa aja atas nama lu di website yang lagi terbuka. Ada penipuan yang nyuruh korban nempel kode ke Console supaya akunnya diambil alih. Aturannya sederhana: jangan pernah nempel kode di Console kalau lu nggak ngerti apa yang kode itu lakukan.
