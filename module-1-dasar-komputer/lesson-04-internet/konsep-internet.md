## Apa itu Internet?

Internet = **network of networks**. Miliaran komputer tersambung satu sama lain.

---

### Internet vs WWW (World Wide Web)

Beda tapi sering disama-in:

**Internet**:
- Infrastruktur fisik (kabel, router, server)
- Protocol (TCP/IP, HTTP, FTP, etc)
- Transport layer

**WWW (Web)**:
- Aplikasi yang jalan di atas internet
- Website, browser
- HTTP protocol

**Analogi**: Internet = jalan raya, WWW = mobil yang jalan di atas jalan raya.

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

**Client** = yang minta data (browser lu, app mobile)  
**Server** = yang kasih data (Google server, Instagram server)

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

Data ga dikirim utuh. Dipecah jadi **packet** kecil-kecil, dikirim terpisah, terus digabung lagi di tujuan.

**Analogy**: Kirim buku 1000 halaman lewat pos. Daripada 1 paket gede (berat, lama), dipecah jadi 10 paket masing-masing 100 halaman. Tiap paket jalan sendiri, sampe tujuan digabung lagi.

**Kenapa?**
- Lebih efisien
- Kalau 1 packet hilang, tinggal kirim ulang yang itu doang
- Bisa lewat route berbeda (load balancing)

---

### Router

Router = **traffic director** internet.

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

Protocol = **aturan komunikasi**.

**Analogi**: Lu telepon temen. Ada etika:
- "Halo" dulu
- Tunggu jawaban
- Ngobrol
- "Bye" sebelum tutup

Internet juga gitu. Ada protocol:
- **TCP/IP**: Base protocol buat semua komunikasi
- **HTTP/HTTPS**: Web browsing
- **FTP**: File transfer
- **SMTP**: Email
- **WebSocket**: Real-time communication (chat, game)

---

### Bandwidth vs Latency

**Bandwidth** = seberapa banyak data bisa lewat (Mbps, Gbps)  
**Latency** = seberapa cepat data sampe (ms)

**Analogi**: Pipa air
- Bandwidth = diameter pipa (besar = banyak air lewat)
- Latency = jarak rumah ke sumber air (jauh = lama sampe)

**Gaming** butuh **low latency** (ping kecil), bandwidth ga perlu gede.  
**Streaming 4K** butuh **high bandwidth**, latency agak tinggi ga masalah.

---

Next: **HTTP** - protocol buat browsing web.
