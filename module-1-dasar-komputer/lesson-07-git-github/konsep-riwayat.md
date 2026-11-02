## Riwayat dan Membatalkan Perubahan

### Menambah commit kedua

Tambah satu baris ke `menu.txt`:

```bash
echo "Mie goreng 13000" >> menu.txt
```

Dua tanda `>>` artinya menambah ke akhir file. Kalau cuma satu `>`, isi file lama ketimpa. Ini sering bikin orang kaget.

Sebelum commit, lihat apa yang berubah:

```bash
git diff
```

Hasilnya kira-kira:

```
+Mie goreng 13000
```

Baris yang diawali `+` adalah baris yang ditambah. Baris yang diawali `-` adalah yang dihapus. Setelah yakin, commit:

```bash
git add menu.txt
git commit -m "Tambah mie goreng"
```

### Melihat riwayat

```bash
git log --oneline
```

Hasilnya kira-kira:

```
72dcdcd Tambah mie goreng
7b02492 Tambah menu pertama
```

Tiap baris adalah satu commit. Kode di depan (`72dcdcd`) adalah ID-nya. ID lu akan beda dengan contoh ini, dan itu normal. Yang terbaru ada di atas.

### Membatalkan perubahan yang belum di-commit

Misalnya lu iseng nambah baris yang ternyata salah:

```bash
echo "Es teh 40000" >> menu.txt
```

Harganya kebanyakan nol, dan lu mau balik ke kondisi commit terakhir:

```bash
git restore menu.txt
```

Isi `menu.txt` kembali seperti commit terakhir. Perhatikan: perintah ini **menghapus perubahan lu dan nggak bisa dibatalkan**, karena perubahan itu memang belum pernah disimpan Git. Pakai dengan sadar.

### Membatalkan commit yang sudah ada

Kalau yang salah sudah terlanjur di-commit, pakai `git revert`:

```bash
git revert HEAD
```

`HEAD` artinya commit paling atas. Git bakal buka editor buat pesan commit. Simpan dan tutup saja, atau tambah `--no-edit` supaya langsung jalan.

`revert` nggak menghapus commit lama. Dia bikin commit baru yang isinya kebalikan dari commit itu. Jadi riwayat tetap utuh dan ada catatan bahwa lu pernah membatalkan sesuatu. Mirip koreksi di buku kasbon: salah catat nggak disobek halamannya, tapi ditambah baris koreksi.

### Ringkasan perintah

| Mau apa | Perintah |
|---|---|
| Lihat file mana yang berubah | `git status` |
| Lihat isi perubahannya | `git diff` |
| Lihat riwayat | `git log --oneline` |
| Buang perubahan yang belum di-commit | `git restore namafile` |
| Batalkan commit terakhir dengan aman | `git revert HEAD` |
