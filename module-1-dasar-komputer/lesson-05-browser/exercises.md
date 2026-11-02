## Exercises

Kerjain berurutan. Tiap latihan butuh sekitar 5 sampai 10 menit.

---

### Latihan 1: Ganti Teks Halaman

**Tujuan**: terbiasa pakai Inspect Element.

1. Buka `https://example.com`.
2. Klik kanan di judul besar, pilih **Inspect**.
3. Klik dua kali teks di dalam tag `<h1>` dan ganti jadi nama lu.
4. Screenshot hasilnya.
5. Refresh halaman. Apa yang terjadi sama teks tadi?

**Hasil yang benar**: nama lu muncul di halaman, lalu hilang setelah refresh.

---

### Latihan 2: Ubah Warna dengan CSS

**Tujuan**: baca dan ubah aturan CSS.

1. Di halaman yang sama, pilih elemen `<body>` di panel Elements.
2. Di panel Styles, cari aturan `background-color`.
3. Klik nilai warnanya dan ganti ke warna lain.
4. Matiin aturan itu dengan hilangin centangnya, lalu aktifin lagi.

**Hasil yang benar**: warna latar halaman berubah waktu lu ganti nilainya dan balik ke semula waktu aturannya dimatiin.

---

### Latihan 3: Console

**Tujuan**: jalanin JavaScript sederhana dan baca error.

1. Buka tab Console.
2. Ketik `console.log("Halo")` lalu Enter.
3. Ketik `document.body.style.background = "lightyellow"` lalu Enter.
4. Sengaja bikin error: ketik `document.querySelector("h9").textContent`. Tag `h9` nggak ada, jadi hasilnya error.
5. Baca pesan errornya dan jelaskan pakai kata-kata lu sendiri kenapa error itu muncul.

<details>
<summary>Petunjuk</summary>

`querySelector` mengembalikan `null` kalau elemen yang dicari nggak ada. Lalu kode mencoba membaca `textContent` dari `null`.

</details>

---

### Latihan 4: Menghitung Request

**Tujuan**: baca tab Network.

1. Buka salah satu situs berita yang lu kenal.
2. Buka tab Network, lalu refresh halamannya.
3. Catat tiga hal: jumlah request total (ada di bagian bawah panel), ukuran data yang ditransfer, dan waktu sampai halaman selesai dimuat.
4. Filter ke **Img**. Gambar mana yang ukurannya paling besar?

**Hasil yang benar**: lu punya tiga angka dan satu nama file gambar.

---

### Latihan 5: Cari Status Code

**Tujuan**: ngeliat status code HTTP secara langsung.

1. Dengan tab Network terbuka, buka `https://example.com/halaman-yang-tidak-ada`.
2. Cari request utama di daftar. Statusnya apa?
3. Klik request itu dan buka tab **Headers**. Cari baris `Status Code`.

**Hasil yang benar**: status `404`.

---

### Latihan 6: Tampilan Mobile

**Tujuan**: cek tampilan di layar kecil.

1. Buka website sekolah atau kampus lu.
2. Klik ikon Device Toolbar di DevTools.
3. Pilih ukuran iPhone atau Pixel dari dropdown.
4. Catat satu hal yang kelihatan kurang nyaman di layar kecil, misalnya teks terlalu kecil atau menu menumpuk.

**Hasil yang benar**: lu punya satu catatan konkret, misalnya "menu navigasi numpuk dan nggak kebaca", bukan sekadar "kelihatannya biasa aja". Kalau semuanya kelihatan rapi, catat itu juga dan coba satu situs lain.
