## Install Git

Git adalah program yang nyimpen riwayat perubahan di sebuah folder proyek. Bayangin fitur save point di game: lu bisa balik ke kondisi mana pun yang pernah disimpan. Di course ini kita cuma pasang dan atur dulu. Cara pakainya dibahas belakangan.

Git beda dari GitHub. Git adalah program di laptop lu. GitHub adalah website buat nyimpen proyek Git secara online, mirip Google Drive buat kode.

---

### Langkah Install

**macOS**

Buka terminal dan ketik `git --version`. Kalau Git belum ada, macOS akan nawarin install Command Line Tools. Klik Install dan tunggu sampai selesai. Prosesnya bisa belasan menit.

**Windows**

1. Download dari [git-scm.com](https://git-scm.com/).
2. Jalankan installer. Pilihan default aman buat hampir semua langkah, jadi klik Next sampai selesai.
3. Hasilnya, lu dapat **Git Bash**, terminal bergaya Mac / Linux yang lebih enak dipakai buat belajar.

**Linux (Ubuntu / Debian)**

```bash
sudo apt install git
```

---

### Cek Hasilnya

Buka terminal baru (Windows: Git Bash), lalu ketik:

```bash
git --version
```

Hasil yang benar: `git version 2.x.x`.

### Atur Nama dan Email

Git mencatat siapa yang bikin tiap perubahan, jadi lu perlu ngasih tau identitas lu:

```bash
git config --global user.name "Nama Lu"
git config --global user.email "emaillu@example.com"
```

Cek hasilnya:

```bash
git config --list
```

Cari dua baris `user.name` dan `user.email` di hasilnya.

### Akun GitHub

Bikin akun gratis di [github.com](https://github.com/). Pakai email yang sama dengan yang lu masukin di `user.email` biar riwayat perubahan lu terhubung ke akun itu.

Pilih username yang netral dan layak dipakai buat profil kerja, karena nanti nama itu bakal kelihatan di CV dan portofolio.
