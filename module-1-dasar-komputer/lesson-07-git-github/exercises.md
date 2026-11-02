## Exercises: Git dan GitHub

Ketik sendiri, jangan copy-paste. Semua latihan dikerjakan di dalam terminal.

---

### Latihan 1: Repo pertama

**Tujuan**: Bikin repo dan commit pertama.

**Yang perlu lu lakukan**:
1. Bikin folder `catatan-belajar` di Desktop dan masuk ke dalamnya.
2. Jalankan `git init`.
3. Bikin file `hari-1.txt` yang isinya satu kalimat tentang apa yang lu pelajari hari ini.
4. Jalankan `git status` dan perhatikan file itu masuk bagian mana.
5. `git add`, lalu `git commit` dengan pesan yang jelas.
6. Jalankan `git status` lagi.

**Hasil yang benar**: Langkah terakhir menampilkan `nothing to commit, working tree clean`.

---

### Latihan 2: Tiga commit, satu riwayat

**Tujuan**: Terbiasa dengan alur ubah, add, commit.

**Yang perlu lu lakukan**:
1. Tambah satu baris ke `hari-1.txt` pakai `>>`.
2. Jalankan `git diff` dan baca hasilnya.
3. Commit.
4. Bikin file `hari-2.txt`, lalu commit.
5. Jalankan `git log --oneline`.

**Hasil yang benar**: `git log --oneline` menampilkan tiga commit, dengan pesan yang bisa lu pahami tanpa buka filenya.

---

### Latihan 3: Membatalkan

**Tujuan**: Tahu bedanya membatalkan yang belum dan yang sudah di-commit.

**Yang perlu lu lakukan**:
1. Tambah baris asal-asalan ke `hari-1.txt`, tanpa commit.
2. Jalankan `git restore hari-1.txt` dan cek isi filenya.
3. Tambah baris salah lagi, kali ini commit.
4. Jalankan `git revert HEAD --no-edit`.
5. Jalankan `git log --oneline` dan perhatikan commit baru yang muncul.

**Hasil yang benar**: Setelah langkah 2, baris asal-asalan hilang. Setelah langkah 5, riwayat punya satu commit tambahan bernama `Revert ...`, dan isi file kembali seperti sebelum commit yang salah.

---

### Latihan 4: Branch

**Tujuan**: Mencoba perubahan tanpa menyentuh `main`.

**Yang perlu lu lakukan**:
1. Bikin branch `coba-catatan` dan pindah ke sana.
2. Bikin file `eksperimen.txt` dan commit.
3. Pindah ke `main` dan jalankan `ls`. File `eksperimen.txt` seharusnya nggak ada.
4. Jalankan `git merge coba-catatan`, lalu `ls` lagi.

**Hasil yang benar**: File muncul di `main` hanya setelah merge.

---

### Latihan 5: Kirim ke GitHub

**Tujuan**: Punya repo di GitHub.

**Yang perlu lu lakukan**:
1. Bikin repo kosong di GitHub bernama `catatan-belajar`.
2. Hubungkan dengan `git remote add origin ...`.
3. Jalankan `git push -u origin main`.
4. Buka halaman repo di browser dan cek riwayat commit-nya.
5. Ubah satu file, commit, lalu `git push` tanpa opsi tambahan.

**Hasil yang benar**: Commit baru terlihat di GitHub.

---

### Latihan 6: Clone

**Tujuan**: Mengambil repo dari GitHub.

**Yang perlu lu lakukan**:
1. Pindah ke folder lain, misalnya `cd ~/Desktop`.
2. Jalankan `git clone` dengan URL repo `catatan-belajar` lu sendiri.
3. Masuk ke folder hasil clone dan jalankan `git log --oneline`.

**Hasil yang benar**: Riwayat commit yang sama dengan yang di laptop lu muncul di folder baru.

Kalau macet di login saat push, baca bagian Kesalahan Umum.
