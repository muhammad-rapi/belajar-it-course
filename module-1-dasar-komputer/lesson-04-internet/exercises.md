## Exercises

Empat latihan, masing-masing sekitar 5 sampai 10 menit. Semuanya dijalankan di terminal. Di Windows, pakai PowerShell atau Git Bash.

---

### Latihan 1: Cari IP dari Nama Domain

**Tujuan**: pakai DNS lewat terminal.

```bash
nslookup github.com
```

Cari baris `Address` setelah bagian `Name`. Itu IP address github.com.

**Tugas**: lakukan hal yang sama buat tiga domain lain yang lu pilih sendiri.

**Hasil yang benar**: lu punya IP buat tiap domain. Angka lu bisa beda dari temen lu atau dari contoh di materi. Itu normal, karena situs besar punya banyak server dan DNS ngasih yang terdekat atau yang sedang tersedia.

---

### Latihan 2: Kirim Request dengan curl

**Tujuan**: lihat sendiri permintaan dan balasan HTTP.

```bash
curl https://jsonplaceholder.typicode.com/users/1
```

**Hasil yang benar**: balasan berupa data JSON tentang satu pengguna, berisi `id`, `name`, dan `email`.

Lalu lihat header-nya saja:

```bash
curl -I https://example.com
```

**Hasil yang benar**: baris pertamanya `HTTP/2 200` (atau `HTTP/1.1 200 OK`), diikuti header seperti `content-type`.

---

### Latihan 3: Status Code

**Tujuan**: kenal status code lewat contoh langsung.

Jalankan dua perintah ini dan perhatikan status code-nya:

```bash
curl -I https://example.com
curl -I https://example.com/halaman-yang-tidak-ada
```

**Hasil yang benar**: yang pertama `200`, yang kedua `404`. Jelasin pakai kata-kata lu sendiri kenapa angkanya beda.

---

### Latihan 4: Kirim POST

**Tujuan**: bedain GET dan POST.

```bash
curl -X POST https://jsonplaceholder.typicode.com/posts \
  -H "Content-Type: application/json" \
  -d '{"title": "Test", "body": "Halo", "userId": 1}'
```

**Hasil yang benar**: balasan JSON yang isinya sama dengan yang lu kirim, ditambah `"id": 101`. Situs ini cuma buat latihan, jadi datanya nggak benar-benar disimpan.

Di Windows PowerShell, `curl` bisa berarti perintah lain. Kalau perintah di atas error, pakai Git Bash atau tulis `curl.exe` sebagai gantinya.

---

### Opsional: Lihat Rute Paket

```bash
traceroute google.com      # macOS dan Linux
tracert google.com         # Windows
```

Hitung berapa lompatan (hop) sampai tujuan. Sebagian baris bisa menampilkan `* * *`, artinya router di titik itu nggak membalas. Itu normal.

Hasilnya beda buat tiap orang, karena tergantung ISP dan lokasi lu.
