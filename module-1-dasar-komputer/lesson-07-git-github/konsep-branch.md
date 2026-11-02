## Branch

### Masalahnya

Lu punya versi menu yang sudah jalan dan rapi. Lu mau nyoba nambah daftar minuman, tapi belum yakin hasilnya bagus. Kalau langsung diubah di versi utama dan ternyata berantakan, lu harus beresin sendiri.

### Cara kerja branch

Branch itu jalur terpisah. Bayangin lu fotokopi buku resep, lalu corat-coret di fotokopiannya. Kalau hasilnya bagus, lu pindahin ke buku asli. Kalau jelek, fotokopinya dibuang dan buku asli nggak kena apa-apa.

Jalur utama di Git biasanya bernama `main`. Cek lu ada di branch mana:

```bash
git branch
```

Tanda `*` ada di branch yang sedang dipakai.

### Bikin dan pindah ke branch baru

```bash
git checkout -b tambah-minuman
```

Perintah ini bikin branch `tambah-minuman` sekaligus pindah ke sana. Sekarang tambah isi dan commit seperti biasa:

```bash
echo "Es teh 4000" >> menu.txt
git add menu.txt
git commit -m "Tambah es teh"
```

### Pindah balik ke main

```bash
git checkout main
cat menu.txt
```

Perhatikan: baris "Es teh 4000" nggak ada di `main`. Perubahan itu cuma ada di branch `tambah-minuman`. Itu fungsi branch.

### Gabungkan kalau sudah yakin

```bash
git merge tambah-minuman
cat menu.txt
```

Sekarang `main` ikut punya baris es teh. Proses ini namanya **merge**.

Kalau yang lu ubah di dua branch adalah baris yang sama, Git nggak bisa memilih sendiri dan bakal bilang ada **conflict**. Itu bukan error yang merusak apa-apa. Git cuma minta lu yang menentukan versi mana yang dipakai. Cara menyelesaikannya dibahas di lesson lanjutan. Untuk sekarang, kalau lu kerja sendirian di satu branch, hampir nggak bakal ketemu.

### Kapan pakai branch

- Mau nyoba sesuatu yang belum pasti
- Mengerjakan satu fitur yang butuh beberapa commit
- Kerja bareng orang lain, supaya perubahan masing-masing nggak saling tabrakan
