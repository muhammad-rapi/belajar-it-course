## Exercises

Ketik sendiri, jangan copy-paste. Tiap latihan sekitar 5 sampai 10 menit. Di Windows, pakai Git Bash supaya perintahnya sama dengan contoh.

---

### Latihan 1: Pindah-pindah Folder

**Tujuan**: pindah folder dan cek posisi.

1. Buka terminal.
2. Jalankan `pwd` buat lihat posisi lu.
3. Jalankan `cd ~` buat balik ke home.
4. Pindah ke Desktop dengan `cd Desktop`, lalu lihat isinya dengan `ls`.
5. Balik ke home lagi dan jalankan `pwd`.

**Hasil yang benar**: semua perintah jalan tanpa error, dan `pwd` terakhir nunjukin folder home lu.

---

### Latihan 2: Bikin Folder Proyek

**Tujuan**: bikin struktur folder dari terminal.

Targetnya:

```
belajar-python/
├── src/
├── tests/
└── docs/
```

Jalankan:

```bash
cd ~/Desktop
mkdir belajar-python
cd belajar-python
mkdir src tests docs
ls
```

**Hasil yang benar**: `ls` nampilin `docs  src  tests`.

---

### Latihan 3: Bikin File

**Tujuan**: bikin file di dalam folder.

Lanjut dari latihan 2:

```bash
cd src
touch main.py utils.py
ls
```

**Hasil yang benar**: `ls` nampilin `main.py  utils.py`.

---

### Latihan 4: Salin dan Pindah

**Tujuan**: bedain `cp` dan `mv`.

Masih di folder `src`:

```bash
cp main.py backup.py
ls
mv backup.py ../tests/
ls
cd ../tests
ls
```

**Hasil yang benar**:

- Setelah `cp`, `ls` nampilin tiga file: `backup.py  main.py  utils.py`.
- Setelah `mv`, `ls` di `src` cuma nampilin `main.py  utils.py`.
- `ls` di `tests` nampilin `backup.py`.

Perhatikan bedanya: `cp` bikin salinan, `mv` mindahin file aslinya.

---

### Latihan 5: Path Relatif

**Tujuan**: pindah antar folder tanpa nulis path lengkap.

Dari folder `tests`:

```bash
pwd
cd ../src
pwd
cd ../docs
pwd
```

**Hasil yang benar**: tiap `pwd` nampilin folder yang sesuai (`tests`, `src`, lalu `docs`), semuanya di dalam `belajar-python`.

**Tantangan**: dari `docs`, pindah ke `tests` dalam satu perintah.

<details>
<summary>Jawaban</summary>

```bash
cd ../tests
```

</details>

---

### Latihan 6: Rapikan dan Hapus

**Tujuan**: pakai `rm` dengan sadar.

1. Balik ke Desktop: `cd ~/Desktop`.
2. Cek dulu isi yang mau dihapus: `ls belajar-python`.
3. Hapus: `rm -r belajar-python`.
4. Cek: `ls`. Folder `belajar-python` seharusnya sudah nggak ada.

Perhatikan: `rm` nggak ngirim ke Recycle Bin atau Trash. Kebiasaan yang baik: jalankan `ls` dulu buat memastikan lu menghapus folder yang benar.

---

### Cek Diri

- Lu bisa buka terminal tanpa bingung.
- Lu paham `pwd`, `cd`, `ls`, `mkdir`, `touch`, `rm`, `cp`, dan `mv`.
- Lu bisa pindah folder pakai path relatif (`..` dan `.`).

Kalau ada yang masih ragu, ulangi latihannya. Kalau macet, buka bagian Kesalahan Umum.
