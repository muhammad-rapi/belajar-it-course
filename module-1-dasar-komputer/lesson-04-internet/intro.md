## Kenapa Perlu Paham Internet

Lu pakai internet tiap hari: browsing, streaming, chat. Tapi kebanyakan orang nggak tahu apa yang terjadi di antara "tekan Enter" dan "halaman muncul".

### Masalah Kalau Nggak Paham

**1. Bingung waktu muncul error.**

```
ERR_CONNECTION_REFUSED
DNS_PROBE_FINISHED_NXDOMAIN
504 Gateway Timeout
```

Tanpa paham internet, yang bisa lu lakuin cuma restart router. Dengan paham, lu tahu masalahnya di sisi mana.

**2. Susah bikin aplikasi yang terhubung ke internet.** Aplikasi chat ngirim pesan ke server. Toko online ngambil data produk dari database. Semuanya pakai pola permintaan dan balasan yang sama.

**3. Debugging jadi tebak-tebakan.**

```python
response = requests.get("https://api.example.com/data")
print(response.status_code)  # 404
```

Lu perlu tahu 404 itu artinya apa dan kenapa muncul.

### Analogi: Kantor Pos

Bayangin lu kirim surat ke temen:

1. Lu tulis surat (data).
2. Lu masukin amplop dan tulis alamat (IP address).
3. Lu kasih ke kantor pos (router).
4. Kantor pos nganterin ke alamat tujuan.
5. Temen lu baca, lalu balas.
6. Balasan sampai ke lu.

Internet bekerja mirip. Komputer lu adalah pengirim, server adalah penerima, dan router adalah kantor pos.

### Yang Bakal Lu Bisa

- Bedain internet dan web
- Jelasin apa itu IP address dan router
- Baca permintaan dan balasan HTTP, termasuk status code
- Jelasin kerja DNS
- Kirim permintaan HTTP dan cek DNS dari terminal

Kita mulai dari yang paling dasar: apa sebenarnya internet itu.
