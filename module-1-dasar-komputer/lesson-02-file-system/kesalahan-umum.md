## Kesalahan Umum

### 1. Mengira Ekstensi Bisa Diganti Begitu Saja

Gejalanya: lu ganti nama `catatan.txt` jadi `catatan.docx`, lalu Word bilang file-nya rusak.

Ganti ekstensi nggak mengubah isi file. Isinya tetap teks biasa, sementara `.docx` butuh format khusus. Kalau mau mengubah format, buka file di aplikasinya lalu pakai Save As atau Export.

### 2. Menyembunyikan Ekstensi

Gejalanya: lu klik file yang namanya `tugas.pdf`, tapi ternyata program berbahaya. Di komputer lu, ekstensi aslinya `.exe` dan nggak kelihatan.

Nyalain tampilan ekstensi sekarang juga. Caranya ada di materi File dan Ekstensi.

### 3. Salah Pakai Garis Miring

Gejalanya: kode atau perintah yang lu salin dari tutorial Mac nggak jalan di Windows, atau sebaliknya.

Windows pakai `\`, macOS dan Linux pakai `/`. Di banyak bahasa pemrograman, termasuk Python, garis miring biasa (`/`) tetap jalan di Windows, jadi itu pilihan paling aman buat kode yang mau dipakai lintas sistem.

### 4. Spasi di Nama File dan Folder

Gejalanya: di terminal, `cd Belajar Python` malah error `too many arguments` atau pindah ke tempat yang salah.

Terminal membaca spasi sebagai pemisah antar bagian perintah, jadi `Belajar` dan `Python` dianggap dua hal berbeda. Ada dua jalan keluar:

- Bungkus nama dengan tanda kutip: `cd "Belajar Python"`
- Lebih baik lagi, hindari spasi dari awal. Pakai tanda hubung, misalnya `belajar-python`.

### 5. Path Relatif Dijalankan dari Folder yang Salah

Gejalanya: `FileNotFoundError` padahal file-nya jelas ada.

Path relatif dihitung dari folder tempat program dijalankan, bukan dari lokasi file kodenya. Cek dulu posisi lu pakai `pwd` (macOS dan Linux) atau `cd` (Windows CMD). Dari situ, hitung ulang path-nya.

### 6. `chmod 777` Biar Cepat

Gejalanya: ada error `Permission denied`, lalu lu nemu saran di internet buat `chmod 777`.

Itu jalan pintas yang membuka akses ke semua orang. Cari tahu dulu izin apa yang kurang. Kalau script nggak bisa dijalankan, biasanya cukup `chmod +x`.

### 7. Nyimpen Semua di Satu Folder

Gejalanya: Downloads isinya ratusan file, dan lu nggak ingat mana yang masih penting.

Bikin kebiasaan memindahkan file ke folder yang jelas begitu selesai dipakai. Struktur sederhana sudah cukup: satu folder per proyek, satu folder per mata kuliah atau topik.
