## Exercises

Enam latihan. Tiap latihan sekitar 5 sampai 10 menit. Latihan 4 dan 5 pakai terminal, jadi buat Windows ikuti catatan di tiap latihan.

---

### Latihan 1: Cari Alamat Folder Penting

**Tujuan**: tahu path absolut dari folder yang sering lu pakai.

1. Buka File Explorer (Windows) atau Finder (macOS).
2. Masuk ke folder **Downloads** lu.
3. Cari path lengkapnya:
   - Windows: klik di address bar, path-nya jadi teks.
   - macOS: klik kanan folder Downloads, tekan tombol `Option`, lalu pilih **Copy "Downloads" as Pathname**.
4. Tulis path itu di catatan lu. Lakukan hal yang sama buat Documents dan Desktop.

**Hasil yang benar**: lu punya tiga path absolut. Di Windows bentuknya seperti `C:\Users\namalu\Downloads`, di macOS seperti `/Users/namalu/Downloads`.

---

### Latihan 2: Path Absolut dan Relatif

**Tujuan**: bisa nulis dua jenis path buat file yang sama.

Bikin struktur ini di Desktop (boleh pakai File Explorer atau Finder, file kosong cukup):

```
MyProject/
├── src/
│   └── main.py
└── data/
    └── input.csv
```

Jawab pertanyaan ini:

1. Apa path absolut `main.py` dan `input.csv` di komputer lu?
2. Kalau lu lagi ada di dalam folder `src`, apa path relatif ke `input.csv`?
3. Kalau lu lagi ada di dalam folder `data`, apa path relatif ke `main.py`?

<details>
<summary>Jawaban</summary>

1. Contoh di macOS: `/Users/namalu/Desktop/MyProject/src/main.py`. Di Windows: `C:\Users\namalu\Desktop\MyProject\src\main.py`. Ganti `namalu` dengan nama pengguna lu.
2. `../data/input.csv`. Naik satu level dari `src` ke `MyProject`, lalu masuk `data`.
3. `../src/main.py`. Naik satu level dari `data` ke `MyProject`, lalu masuk `src`.

</details>

---

### Latihan 3: Ekstensi File

**Tujuan**: terbiasa ngelihat ekstensi dan mengenali jenis file.

1. Nyalain tampilan ekstensi (caranya ada di materi File dan Ekstensi).
2. Buka folder Downloads atau Documents.
3. Ambil 10 file dan kelompokkan berdasarkan ekstensinya: dokumen, gambar, arsip, program, atau lainnya.
4. Cari satu file yang ekstensinya belum lu kenal, lalu cari tahu itu file apa.

**Hasil yang benar**: lu punya daftar 10 file yang sudah dikelompokkan dan satu ekstensi baru yang lu pahami.

---

### Latihan 4: Permissions (macOS dan Linux)

**Tujuan**: ngeliat sendiri permissions bekerja.

Windows: latihan ini bisa dilewati. Kalau lu pakai Git Bash, perintahnya sama.

Ketik satu per satu:

```bash
cd ~/Desktop
echo "Hello" > test.txt
ls -l test.txt
chmod 444 test.txt
ls -l test.txt
echo "Test" >> test.txt
chmod 644 test.txt
echo "Test" >> test.txt
cat test.txt
```

Perhatikan hasil tiap langkah.

**Hasil yang benar**:

- Setelah `chmod 444`, `ls -l` nunjukin `-r--r--r--`.
- Perintah `echo "Test" >> test.txt` yang pertama gagal dengan pesan `Permission denied`.
- Setelah `chmod 644`, perintah yang sama berhasil, dan `cat test.txt` nampilin `Hello` lalu `Test`.

Terakhir, hapus file latihan: `rm test.txt`.

---

### Latihan 5: Bikin Struktur Proyek Web

**Tujuan**: bikin banyak folder dan file sekaligus lewat terminal.

Targetnya struktur ini:

```
my-website/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── script.js
└── images/
    └── logo.png
```

Coba bikin dulu sendiri lewat terminal sebelum lihat jawaban.

<details>
<summary>Jawaban (macOS, Linux, Git Bash)</summary>

```bash
mkdir -p ~/Desktop/my-website/{css,js,images}
cd ~/Desktop/my-website
touch index.html css/style.css js/script.js images/logo.png
ls -R
```

`mkdir -p` bikin folder beserta folder induknya. Bagian `{css,js,images}` bikin tiga folder sekaligus. `ls -R` nampilin isi semua subfolder.

</details>

<details>
<summary>Jawaban (Windows PowerShell)</summary>

```powershell
mkdir "$HOME\Desktop\my-website\css", "$HOME\Desktop\my-website\js", "$HOME\Desktop\my-website\images"
cd "$HOME\Desktop\my-website"
New-Item index.html, css\style.css, js\script.js, images\logo.png
```

</details>

---

### Latihan 6: Cari File yang Hilang

**Tujuan**: pakai path buat nyelesaiin masalah yang sering muncul waktu coding.

Skenario: ada program Python di `MyProject/src/main.py` yang mencoba membaca `data/input.csv` seperti ini:

```python
file = open("data/input.csv")
```

Program dijalankan dari dalam folder `src`, dan hasilnya error `FileNotFoundError`.

Jawab:

1. Kenapa error?
2. Tulis dua cara memperbaikinya.

<details>
<summary>Jawaban</summary>

1. Python mencari `data/input.csv` dari folder tempat program dijalankan, yaitu `src`. Di dalam `src` nggak ada folder `data`. Folder `data` ada di satu level di atasnya.
2. Cara pertama pakai path relatif yang benar: `open("../data/input.csv")`. Cara kedua pakai path absolut, misalnya `open("/Users/namalu/Desktop/MyProject/data/input.csv")`. Path absolut jalan dari mana saja, tapi nggak bisa dipindah ke komputer lain tanpa diubah.

</details>
