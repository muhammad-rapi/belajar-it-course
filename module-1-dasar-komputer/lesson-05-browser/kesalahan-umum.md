## Kesalahan Umum

### 1. Mengira perubahan di DevTools disimpan

Lu ganti warna tombol, hasilnya bagus, lalu lu tutup browser. Besoknya tampilan balik seperti semula. Itu normal. DevTools cuma ngubah salinan halaman di browser lu. Kalau mau perubahan permanen, ubah file aslinya di editor, lalu simpan.

Cara aman: setelah nemu CSS yang cocok di DevTools, salin nilainya ke file CSS lu.

### 2. Lupa refresh pas ngecek perubahan

Lu udah ubah file CSS dan simpan, tapi di browser nggak ada yang berubah. Sering kali browser masih nyimpen versi lama (cache). Coba `Cmd + Shift + R` / `Ctrl + Shift + R` buat refresh tanpa cache.

### 3. Buka tab Network setelah halaman selesai dimuat

Daftar request-nya kosong dan lu bingung. Tab Network cuma ngerekam request yang terjadi selama tab itu terbuka. Buka dulu tab-nya, baru refresh halaman.

### 4. Panik liat banyak pesan merah di Console

Hampir semua website punya beberapa peringatan atau error di Console, termasuk website besar. Nggak semuanya penting. Fokus ke error yang muncul bersamaan dengan masalah yang lu alamin, dan baca pesan paling atasnya dulu.

### 5. Nempel kode asing di Console

Udah dibahas di materi Inspect: jangan nempel kode di Console kalau lu nggak ngerti isinya.
