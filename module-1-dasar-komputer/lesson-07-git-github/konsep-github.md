## GitHub: Naruh Proyek di Online

Sampai sekarang semuanya ada di laptop lu. Kalau laptopnya rusak atau hilang, riwayatnya ikut hilang. GitHub nyimpen salinannya di internet, dan itu juga yang dilihat orang lain waktu lu ngasih link portofolio.

### Langkah 1: Bikin repo kosong di GitHub

1. Login ke [github.com](https://github.com/).
2. Klik tombol **New** (atau ikon plus di pojok kanan atas, lalu **New repository**).
3. Isi nama, misalnya `warung-catatan`.
4. Pilih **Public** atau **Private**. Untuk latihan, Private juga boleh.
5. Jangan centang pilihan untuk bikin README, .gitignore, atau license. Repo harus kosong, karena isinya bakal datang dari laptop lu.
6. Klik **Create repository**.

GitHub nampilin halaman dengan URL repo, bentuknya `https://github.com/usernamelu/warung-catatan.git`. Salin URL itu.

### Langkah 2: Hubungkan repo di laptop ke GitHub

Di terminal, di dalam folder `warung-catatan`:

```bash
git remote add origin https://github.com/usernamelu/warung-catatan.git
```

Ganti `usernamelu` dengan username GitHub lu. `origin` cuma nama panggilan untuk alamat itu. Hampir semua orang pakai nama yang sama.

### Langkah 3: Kirim

```bash
git push -u origin main
```

Pertama kali, Git minta login. GitHub sudah nggak menerima password akun biasa di terminal. Ada dua cara yang umum:

- Pasang **GitHub CLI** dari [cli.github.com](https://cli.github.com/), lalu jalankan `gh auth login` dan ikuti petunjuknya lewat browser.
- Buat **personal access token** di pengaturan akun GitHub, lalu tempel token itu di kolom password.

Cara pertama lebih gampang buat pemula.

Setelah berhasil, refresh halaman repo di GitHub. File dan riwayat commit lu sudah ada di sana.

`-u` cuma perlu dipakai sekali. Setelah itu cukup `git push`.

### Alur harian

```bash
# ubah file
git add .
git commit -m "pesan yang jelas"
git push
```

`git add .` artinya masukin semua file yang berubah ke staging. Praktis, tapi cek `git status` dulu supaya lu nggak ikut memasukkan file yang nggak seharusnya.

### Mengambil proyek orang lain

```bash
git clone https://github.com/username/nama-repo.git
```

Perintah ini nyalin seluruh repo beserta riwayatnya ke laptop lu, jadi folder baru dengan nama repo itu. Kalau di GitHub ada update, ambil dengan `git pull`.

### Jangan kirim yang rahasia

Apa pun yang lu push ke repo Public bisa dibaca semua orang, dan riwayat lama tetap bisa dilihat meski filenya sudah dihapus. Jangan commit password, API key, atau file `.env`. Kalau terlanjur, anggap kuncinya sudah bocor dan ganti kuncinya. Menghapus file saja nggak cukup.

Untuk file yang memang nggak mau dilacak Git, bikin file bernama `.gitignore` dan tulis nama file atau foldernya, satu per baris:

```
.env
node_modules/
.DS_Store
```
