## Commit: Save Point Pertama

Kita bikin satu folder latihan dulu. Isinya daftar menu warung, supaya gampang dibayangkan.

```bash
cd ~/Desktop
mkdir warung-catatan
cd warung-catatan
```

### Langkah 1: Jadikan folder ini repo

```bash
git init
```

Hasilnya kira-kira `Initialized empty Git repository in ...`. Git sekarang mulai memantau folder ini. Dia bikin folder tersembunyi bernama `.git` yang isinya seluruh riwayat. Jangan dihapus dan jangan diutak-atik.

### Langkah 2: Bikin file

Bikin file `menu.txt` isinya satu baris. Pakai VS Code atau perintah ini:

```bash
echo "Nasi goreng 15000" > menu.txt
```

### Langkah 3: Lihat status

```bash
git status
```

Di hasilnya, `menu.txt` muncul di bagian **Untracked files**. Artinya file itu ada di folder, tapi Git belum diminta mencatatnya.

### Langkah 4: Pilih file yang mau dicatat

```bash
git add menu.txt
```

Perintah ini belum menyimpan apa-apa. Dia cuma menaruh `menu.txt` di **staging area**, yaitu tempat nunggu sebelum dicatat. Bayangin lu lagi belanja: `git add` itu masukin barang ke keranjang. Belum dibayar.

Kenapa dibikin dua langkah? Karena kadang lu ubah lima file tapi cuma dua yang berhubungan dengan satu perubahan. Lu bisa masukin dua itu dulu, dan sisanya untuk commit berikutnya.

Cek lagi dengan `git status`. Sekarang `menu.txt` ada di bagian **Changes to be committed**.

### Langkah 5: Commit

```bash
git commit -m "Tambah menu pertama"
```

Bagian setelah `-m` adalah pesan, yaitu catatan singkat tentang apa yang lu ubah. Ini langkah bayar di kasir. Perubahan lu sekarang tersimpan.

Jalankan `git status` sekali lagi. Hasilnya `nothing to commit, working tree clean`. Artinya nggak ada perubahan yang belum tercatat.

### Pesan commit yang berguna

Pesan itu bakal lu baca lagi berbulan-bulan kemudian, jadi tulis yang jelas.

| Kurang berguna | Lebih berguna |
|---|---|
| `update` | `Tambah menu mie goreng` |
| `fix` | `Perbaiki harga es teh yang salah ketik` |
| `asdf` | `Pisahkan menu makanan dan minuman` |

Satu commit sebaiknya satu perubahan yang bisa dijelaskan dalam satu kalimat.

### Alur yang bakal lu ulang terus

```
ubah file  ->  git add  ->  git commit
```

Hampir semua kerja harian dengan Git adalah tiga langkah itu.

Coba perhatikan: `git status` itu murah dan aman. Kalau bingung sedang di kondisi apa, jalankan itu dulu.
