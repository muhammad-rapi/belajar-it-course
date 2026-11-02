## Kesalahan Umum

### 1. Mengira Internet dan Web Itu Sama

Web cuma salah satu layanan yang jalan di atas internet. Email, game online, dan panggilan video juga memakai internet. Kalau ada yang bilang "internetnya mati" padahal WhatsApp jalan, yang bermasalah biasanya bukan internetnya.

### 2. Langsung Nyalahin Internet Waktu Situs Nggak Terbuka

Bedain dulu sumber masalahnya:

- **`DNS_PROBE_FINISHED_NXDOMAIN`**: nama domain nggak ketemu. Cek ejaan alamatnya, atau masalah di DNS.
- **`ERR_CONNECTION_REFUSED`** atau **timeout**: server nggak mau atau nggak sempat menjawab.
- **`404`**: server menjawab, tapi halaman yang diminta nggak ada.
- **`500`, `502`, `503`**: server menjawab, tapi dia sendiri sedang bermasalah.

Kalau status code muncul, berarti koneksi lu sendiri sudah baik. Masalahnya di alamat atau di server.

### 3. Salah Paham Arti 4xx dan 5xx

4xx berarti permintaan dari sisi client yang bermasalah (alamat salah, belum login, nggak punya akses). 5xx berarti server yang bermasalah. Waktu debug API, ini nentuin lu harus memeriksa kode lu sendiri atau menunggu server pulih.

### 4. Ngira `http://` dan `https://` Cuma Beda Huruf

Beda utamanya di enkripsi. Jangan masukin password atau data pembayaran di halaman yang cuma `http://`.

### 5. Menunggu DNS Langsung Berubah

Kalau lu baru ganti DNS record dan situsnya belum berubah, itu wajar. Cache masih menyimpan alamat lama sampai TTL habis. Tunggu, atau kosongkan cache DNS di komputer lu sendiri.

### 6. `curl` Nggak Jalan di Windows

Di PowerShell versi lama, `curl` adalah alias buat perintah lain dan menghasilkan error yang membingungkan. Pakai `curl.exe`, atau pakai Git Bash.

### 7. Menempel Token atau API Key ke Tempat Umum

Waktu nanti lu pakai API yang butuh token, jangan tempel token itu ke chat, forum, atau repo publik. Siapa pun yang punya token itu bisa bertindak atas nama lu.
