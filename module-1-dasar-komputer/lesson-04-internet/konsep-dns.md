## DNS - Domain Name System

DNS = **phonebook internet**. Translate domain (google.com) jadi IP address (142.250.185.46).

---

### Kenapa Perlu DNS?

Komputer cuma ngerti IP address (angka). Tapi manusia susah inget angka.

**Tanpa DNS**: Lu harus hafal
```
142.250.185.46  (Google)
157.240.22.35   (Facebook)
104.244.42.129  (Twitter)
```

**Dengan DNS**: Lu tinggal inget
```
google.com
facebook.com
twitter.com
```

DNS otomatis translate domain → IP.

---

### DNS Lookup Process

**1. Lu ketik google.com di browser**

**2. Browser check cache**
- Ada di browser cache? Pake itu.
- Ada di OS cache? Pake itu.
- Ga ada? Lanjut step 3.

**3. Browser tanya DNS Resolver** (biasanya ISP lu atau 8.8.8.8)

**4. Resolver tanya Root DNS Server**
- "Siapa yang handle .com?"
- Root: "Tanya TLD Server .com"

**5. Resolver tanya TLD (Top-Level Domain) Server**
- "Siapa yang handle google.com?"
- TLD: "Tanya Authoritative DNS Server google"

**6. Resolver tanya Authoritative DNS**
- "IP google.com apa?"
- Auth: "142.250.185.46"

**7. Resolver kasih IP ke browser**

**8. Browser konek ke 142.250.185.46**

**Proses ini cepet** (milidetik) karena cache di tiap layer.

---

### DNS Record Types

**A Record** = Domain → IPv4
```
google.com → 142.250.185.46
```

**AAAA Record** = Domain → IPv6
```
google.com → 2001:4860:4860::8888
```

**CNAME** = Alias
```
www.google.com → google.com
```

**MX Record** = Mail server
```
gmail.com → mail.google.com
```

**TXT Record** = Text data (verification, SPF, etc)
```
google.com → "v=spf1 include:_spf.google.com ~all"
```

---

### Public DNS Servers

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

**Kenapa ganti DNS?**
- ISP DNS lambat → pake Google/Cloudflare lebih cepet
- ISP block site tertentu → public DNS ga block
- Privacy (Cloudflare claim ga log data)

---

### DNS Cache

**Browser cache**: ~60 detik  
**OS cache**: ~beberapa menit  
**Router cache**: ~beberapa jam  

**Flush DNS cache** (kalau web ga load setelah update DNS):

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

### DNS Lookup Tools

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

**dig** (detail):
```bash
dig google.com
```

**host**:
```bash
host google.com
```

---

### DNS Propagation

Kalau lu update DNS record (misal: ganti IP server), ga langsung update global.

**Propagation time**: 24-48 jam

Karena cache di tiap layer. TTL (Time To Live) nentuin berapa lama cache.

**Check propagation**:
- [whatsmydns.net](https://www.whatsmydns.net/)
- Liat DNS dari berbagai lokasi global

---

Next: **Exercises** - praktek DNS lookup, HTTP request.
