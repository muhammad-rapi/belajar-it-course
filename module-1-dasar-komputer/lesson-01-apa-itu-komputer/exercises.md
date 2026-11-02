## Exercises

Tiga latihan. Tiap latihan sekitar 10 sampai 15 menit.

---

### Latihan 1: Cek Spesifikasi Komputer Lu

**Tujuan**: tahu isi komputer lu sendiri.

**Windows**
1. Buka Task Manager (`Ctrl + Shift + Esc`), lalu tab **Performance**.
2. Catat model CPU dan jumlah core, total RAM, serta jenis dan ukuran disk.
3. Buat cek tambahan: Settings, System, About.

**macOS**
1. Klik menu Apple, lalu **About This Mac**. Catat chip, memori, dan storage.
2. Buka **Activity Monitor** lewat Spotlight buat lihat pemakaian CPU, memori, dan disk.

**Hasil yang benar**: lu punya catatan seperti ini (isinya beda buat tiap komputer):

```
CPU: Intel Core i5, 4 core
RAM: 8 GB
Storage: 256 GB SSD
```

<details>
<summary>Petunjuk</summary>

Task Manager dan Activity Monitor sudah ada di OS, jadi nggak perlu install apa pun. Kalau Windows lu nampilin "Disk 0 (SSD)" atau "(HDD)", itu jawaban jenis storage-nya.

</details>

---

### Latihan 2: Lihat Pemakaian Resource

**Tujuan**: ngeliat sendiri aplikasi mana yang berat.

1. Buka Task Manager atau Activity Monitor dan catat angka awal CPU dan RAM saat komputer lagi santai.
2. Buka Chrome dengan satu tab kosong, lalu catat angkanya lagi.
3. Buka 10 tab (misalnya YouTube dan beberapa situs berita), catat lagi.
4. Buka VS Code atau aplikasi lain yang biasa lu pakai, catat lagi.
5. Urutkan proses berdasarkan memori. Aplikasi mana di urutan teratas?

**Hasil yang benar**: lu punya empat catatan angka dan satu nama aplikasi yang paling banyak makan memori. Angkanya beda-beda tiap komputer, jadi yang penting polanya: tiap aplikasi baru nambah pemakaian RAM, dan tab browser lumayan banyak makan memori.

<details>
<summary>Petunjuk</summary>

Browser biasanya menjalankan tiap tab sebagai proses terpisah, jadi total memorinya bisa besar. Di Task Manager, lihat bagian **Processes** dan klik kolom **Memory** buat mengurutkan.

</details>

---

### Latihan 3: Jelajahi Struktur Folder

**Tujuan**: tahu di mana file lu sebenarnya tersimpan.

1. Buka File Explorer (Windows) atau Finder (macOS).
2. Cari folder **Documents**, **Downloads**, dan **Desktop** milik lu.
3. Bikin folder baru di Documents bernama `test-folder`.
4. Di dalamnya, bikin file teks `hello.txt` yang isinya "Hello".
5. Salin `hello.txt` ke Downloads, lalu hapus yang ada di `test-folder`.
6. Cek Downloads. File hasil salinan harusnya masih ada.

**Hasil yang benar**: `hello.txt` ada di Downloads dan sudah nggak ada di `test-folder`.

<details>
<summary>Petunjuk</summary>

Menyalin dan memindahkan itu beda. Salin bikin dua file, pindah cuma menggeser satu file ke tempat lain. Di Lesson 2 kita bahas alamat file (path) lebih detail.

</details>

---

### Tebak Sendiri

Setelah semua latihan, coba jawab pakai kata-kata lu sendiri:

1. Kenapa komputer jadi lambat waktu RAM hampir penuh?
2. Kenapa file yang lu ketik tapi belum disimpan bisa hilang waktu komputer mati mendadak?

Jawabannya ada di bagian RAM dan storage tadi.
