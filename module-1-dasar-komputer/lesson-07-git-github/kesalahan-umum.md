## Kesalahan Umum

### 1. Lupa `git add` sebelum commit

Gejalanya: lu commit, tapi hasilnya `nothing added to commit` atau perubahan lu nggak ikut tersimpan.

Penyebab: `commit` hanya mencatat apa yang sudah ada di staging. Jalankan `git status`. File di bagian **Changes not staged** belum masuk. Jalankan `git add namafile`, lalu commit lagi.

### 2. Jalankan `git init` di folder yang salah

Gejalanya: lu jalankan `git init` di home atau di Desktop, lalu `git status` menampilkan ratusan file.

Penyebab: Git sekarang memantau seluruh folder itu. Cek dulu pakai `pwd` sebelum `git init`. Kalau terlanjur, hapus folder `.git` di tempat yang salah (`rm -rf .git`, pastikan lu ada di folder yang benar), lalu `git init` di folder proyek.

### 3. Push ditolak karena login

Gejalanya: `Authentication failed` atau Git minta password terus.

Penyebab: GitHub nggak menerima password akun di terminal. Pakai `gh auth login` atau personal access token, seperti di bagian GitHub.

### 4. Pesan error `fatal: not a git repository`

Penyebab: lu ada di folder yang bukan repo. Cek dengan `pwd`, lalu pindah ke folder proyek.

### 5. Branch bernama `master`, bukan `main`

Pada Git versi lama atau konfigurasi tertentu, branch awalnya bernama `master`. Cek dengan `git branch`. Kalau namanya `master`, ganti jadi `main` supaya cocok dengan GitHub:

```bash
git branch -M main
```

### 6. Mem-push file rahasia

Gejalanya: lu sadar sudah commit file `.env` atau password.

Menghapus file di commit berikutnya nggak cukup, karena riwayat lama masih bisa dibaca. Ganti password atau key-nya sekarang. Setelah itu tambahkan nama file ke `.gitignore` supaya nggak keulang.

### 7. Commit semua dengan pesan "update"

Nggak merusak apa-apa, tapi bulan depan lu nggak bakal ngerti riwayat lu sendiri. Biasakan satu commit, satu perubahan, satu pesan yang jelas.
