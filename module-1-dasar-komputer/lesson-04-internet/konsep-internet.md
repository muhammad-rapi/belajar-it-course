## Apa itu Internet

Internet adalah jaringan dari jaringan. Miliaran perangkat tersambung satu sama lain lewat kabel, serat optik, dan sinyal nirkabel.

---

### Internet vs WWW (World Wide Web)

Beda tapi sering disama-in:

**Internet**:
- Infrastruktur fisik: kabel, router, server
- Aturan komunikasi (protokol) seperti TCP/IP

**WWW (web)**:
- Layanan yang berjalan di atas internet
- Website dan browser
- Memakai protokol HTTP

Email dan game online juga memakai internet, tapi bukan bagian dari web.

**Analogi**: internet itu jalan rayanya, web itu salah satu jenis kendaraan yang lewat di atasnya.

---

### IP Address

Setiap device punya **alamat unik**: IP address.

**IPv4** (yang umum):
```
192.168.1.1
142.250.185.46  (google.com)
```

**IPv6** (baru, lebih panjang):
```
2001:4860:4860::8888
```

**Cek IP lu**:

```bash
# macOS/Linux
curl ifconfig.me

# Windows
curl ifconfig.me
# atau
ipconfig
```

---

### Client-Server Model

**Client** adalah pihak yang meminta data (browser lu, aplikasi di HP).  
**Server** adalah pihak yang memberi data (server Google, server Instagram).

**Flow**:
1. Client kirim **request**
2. Server proses
3. Server kirim **response**

**Contoh**: Lu buka google.com
1. Browser (client) kirim request: "Kasih halaman google.com"
2. Google server proses
3. Google server kirim HTML halaman search
4. Browser render halaman

---

### Packet Switching

Data nggak dikirim utuh. Dipecah jadi **packet** kecil-kecil, dikirim terpisah, terus digabung lagi di tujuan.

**Analogi**: kirim buku 1.000 halaman lewat pos. Daripada satu paket besar yang berat, dipecah jadi 10 paket berisi 100 halaman. Tiap paket jalan sendiri, lalu digabung lagi di tujuan.

**Kenapa dipecah?**
- Lebih efisien dipakai bersama banyak pengguna
- Kalau satu paket hilang, cukup kirim ulang yang itu saja
- Paket bisa lewat jalur yang berbeda

---

### Router

Router adalah perangkat yang mengarahkan paket data ke jalur berikutnya, seperti petugas yang ngatur arah kendaraan di persimpangan.

Lu di Jakarta mau akses server di US. Data lu:
1. Keluar dari router rumah
2. Lewat ISP (Indihome, Biznet, dll)
3. Lewat submarine cable (kabel bawah laut)
4. Sampe server US

Tiap hop (lompatan) lewat router yang nge-forward packet ke router berikutnya sampe tujuan.

**Traceroute** (liat route):

```bash
traceroute google.com
# atau di Windows:
tracert google.com
```

Output:
```
1  192.168.1.1  (router rumah)
2  10.0.0.1     (ISP)
3  ...
15 142.250.185.46 (google.com)
```

---

### Protocol

Protokol adalah aturan komunikasi.

**Analogi**: waktu telepon temen, ada urutannya. Bilang "halo", tunggu dijawab, ngobrol, lalu pamit sebelum tutup. Internet juga punya urutan yang disepakati:
- **TCP/IP**: dasar semua komunikasi di internet
- **HTTP dan HTTPS**: buka web
- **FTP**: transfer file
- **SMTP**: kirim email
- **WebSocket**: komunikasi langsung dua arah, dipakai chat dan game

---

### Bandwidth vs Latency

**Bandwidth** adalah seberapa banyak data bisa lewat dalam satu waktu (Mbps, Gbps).  
**Latency** adalah berapa lama data sampai (milidetik).

**Analogi**: pipa air.
- Bandwidth itu besar pipanya. Pipa besar, air yang lewat banyak.
- Latency itu jarak dari sumber air ke rumah lu. Makin jauh, makin lama air pertama sampai.

Game online butuh latency kecil (ping rendah), bandwidth-nya nggak perlu besar. Nonton video 4K butuh bandwidth besar, latency agak tinggi nggak masalah.

---

Berikutnya: HTTP, protokol yang dipakai buat buka web.
