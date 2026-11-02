## DNS

DNS (Domain Name System) adalah buku telepon internet. Tugasnya nerjemahin nama domain seperti `google.com` jadi IP address seperti `142.250.185.46`.

---

### Kenapa Perlu DNS?

Komputer berkomunikasi lewat angka (IP address), sementara manusia lebih gampang ingat nama.

Tanpa DNS, lu harus ngapalin deretan angka tiap situs. Dengan DNS, lu cukup ingat `google.com`, dan DNS yang nyari angkanya. Cara kerjanya sama dengan kontak di HP: lu pilih nama "Ibu", HP yang nelepon nomornya.

---

### Urutan Pencarian DNS

1. Lu ketik `google.com` di browser.
2. Browser ngecek ingatannya (cache). Kalau sudah pernah nyari, dia pakai hasil yang tersimpan. Kalau belum, OS lu ngecek cache-nya juga.
3. Kalau belum ada, permintaan dikirim ke **resolver**, biasanya milik ISP lu atau layanan seperti `8.8.8.8`.
4. Resolver nanya ke **root server**: "siapa yang ngurus `.com`?" Root server nunjuk ke server `.com`.
5. Resolver nanya ke **server `.com`** (disebut TLD server): "siapa yang ngurus `google.com`?" Server itu nunjuk ke server milik Google.
6. Resolver nanya ke **server milik Google** (authoritative server): "IP `google.com` berapa?" Dijawab dengan IP address.
7. Resolver ngasih IP itu ke browser, dan browser tersambung ke server tersebut.

Proses ini hanya makan milidetik karena hasilnya disimpan di tiap tahap.

---

### Jenis Record DNS

**A record**: domain ke IPv4
```
google.com → 142.250.185.46
```

**AAAA record**: domain ke IPv6
```
google.com → 2001:4860:4860::8888
```

**CNAME**: nama alias
```
www.google.com → google.com
```

**MX record**: server email
```
gmail.com → mail.google.com
```

**TXT record**: teks bebas, dipakai buat verifikasi domain dan keamanan email
```
google.com → "v=spf1 include:_spf.google.com ~all"
```

---

### DNS Publik

**Google DNS**:
```
8.8.8.8
8.8.4.4
```

**Cloudflare DNS**:
```
1.1.1.1
1.0.0.1
```

**OpenDNS**:
```
208.67.222.222
208.67.220.220
```

**Kenapa orang ganti DNS?**
- DNS bawaan ISP kadang lambat atau sering bermasalah
- Sebagian ISP memblokir situs lewat DNS-nya
- Alasan privasi: tiap penyedia punya kebijakan pencatatan yang berbeda, jadi baca kebijakannya dulu

---

### Cache DNS

Hasil pencarian DNS disimpan sementara di browser, OS, router, dan resolver. Lama tersimpannya ditentukan oleh **TTL** (Time To Live) yang diatur pemilik domain, dan biasanya antara beberapa menit sampai beberapa jam.

**Mengosongkan cache DNS** (kalau situs belum berubah setelah DNS diganti):

**macOS**:
```bash
sudo dscacheutil -flushcache
sudo killall -HUP mDNSResponder
```

**Windows**:
```bash
ipconfig /flushdns
```

**Linux**:
```bash
sudo systemd-resolve --flush-caches
```

---

### Alat Cek DNS

**nslookup**:
```bash
nslookup google.com
```

Output:
```
Server:  8.8.8.8
Address: 8.8.8.8#53

Name:    google.com
Address: 142.250.185.46
```

**dig** (lebih rinci):
```bash
dig google.com
```

**host**:
```bash
host google.com
```

---

### DNS Propagation

Kalau lu mengubah DNS record (misalnya ganti IP server), perubahannya nggak langsung terlihat di semua tempat.

**Propagation time**: biasanya beberapa menit sampai beberapa jam, kadang sampai sehari lebih

Penyebabnya cache di tiap tahap. Selama TTL belum habis, sebagian orang masih ngeliat alamat lama.

**Cara mengecek**: [whatsmydns.net](https://www.whatsmydns.net/) nampilin hasil DNS dari berbagai lokasi di dunia.

---

Berikutnya: latihan DNS dan HTTP di Exercises.
