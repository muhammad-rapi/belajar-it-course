## HTTP

HTTP (HyperText Transfer Protocol) adalah aturan yang dipakai browser buat minta data ke server dan buat server ngebalas.

---

### Permintaan dan Balasan

**1. Client (browser) kirim permintaan (request)**

```
GET /search?q=python HTTP/1.1
Host: google.com
```

**2. Server memproses lalu kirim balasan (response)**

```
HTTP/1.1 200 OK
Content-Type: text/html

<html>
  <body>Hasil search...</body>
</html>
```

---

### HTTP Methods

**GET**: ambil data (nggak mengubah apa-apa di server)

```
GET /api/users/123
```

Artinya: "kasih data user nomor 123"

**POST**: kirim data baru (bikin)

```
POST /api/users
Body: {"name": "Rafi", "email": "rafi@gmail.com"}
```

Artinya: "bikin user baru dengan data ini"

**PUT**: ganti seluruh data

```
PUT /api/users/123
Body: {"name": "Rafi Updated", "email": "new@gmail.com"}
```

**DELETE**: hapus data

```
DELETE /api/users/123
```

**PATCH**: ubah sebagian data

```
PATCH /api/users/123
Body: {"email": "new@gmail.com"}  # Cuma ganti email
```

---

### HTTP Status Codes

Server ngasih **status code**, yaitu angka yang nunjukin permintaan berhasil atau gagal.

**2xx = Success**
- `200 OK` = Sukses
- `201 Created` = Data baru dibuat (after POST)

**3xx = Redirect**
- `301 Moved Permanently` = URL pindah permanent
- `302 Found` = Temporary redirect

**4xx = kesalahan di sisi client (permintaan lu)**
- `400 Bad Request` = Request salah format
- `401 Unauthorized` = Belum login
- `403 Forbidden` = sudah login, tapi nggak punya akses
- `404 Not Found` = URL nggak ada
- `429 Too Many Requests` = Spam request, kena limit

**5xx = kesalahan di sisi server**
- `500 Internal Server Error` = Server crash
- `502 Bad Gateway` = Gateway/proxy error
- `503 Service Unavailable` = Server down/maintenance
- `504 Gateway Timeout` = Server terlalu lama respond

---

### HTTPS (Secure)

**HTTP** mengirim data sebagai teks biasa, jadi bisa dibaca oleh pihak yang menyadap jaringan.  
**HTTPS** mengenkripsi data (lewat TLS), jadi isinya diacak selama di perjalanan.

**Kenapa penting?**
- Password di form login nggak bisa dibaca orang lain di jaringan yang sama
- Data pembayaran lebih aman
- Pihak yang cuma ngeliat lalu lintas jaringan nggak bisa baca isi halaman yang lu buka

**Cara cek**: alamat web diawali `https://`, dan browser biasanya nampilin ikon gembok.

---

### Headers

Request dan response punya **header**, yaitu keterangan tambahan di luar isi utamanya.

**Request headers**:
```
GET /api/data HTTP/1.1
Host: api.example.com
User-Agent: Mozilla/5.0
Authorization: Bearer contoh-token
Content-Type: application/json
```

**Response headers**:
```
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1234
Set-Cookie: session=abc123
```

**Common headers**:
- `Content-Type`: Format data (JSON, HTML, image)
- `Authorization`: Token login
- `Cookie`: Session data
- `User-Agent`: Info browser/device

---

### Contoh: Memanggil API

**Ambil data user (GET)**:

```bash
curl https://jsonplaceholder.typicode.com/users/1
```

Response:
```json
{
  "id": 1,
  "name": "Leanne Graham",
  "email": "Sincere@april.biz"
}
```

**Bikin post baru (POST)**:

```bash
curl -X POST https://jsonplaceholder.typicode.com/posts \
  -H "Content-Type: application/json" \
  -d '{"title": "Hello", "body": "World", "userId": 1}'
```

Hasilnya (situs ini cuma buat latihan, datanya nggak benar-benar disimpan):
```json
{
  "id": 101,
  "title": "Hello",
  "body": "World",
  "userId": 1
}
```

---

### HTTP/2 & HTTP/3

**HTTP/1.1** adalah versi lama. Satu koneksi menangani satu permintaan pada satu waktu.

**HTTP/2** memungkinkan banyak permintaan jalan bersamaan lewat satu koneksi, jadi halaman dimuat lebih cepat.

**HTTP/3** memakai protokol QUIC dan terutama membantu di koneksi yang kurang stabil, seperti jaringan seluler.

Browser dan server otomatis memilih versi yang terbaik. Lu nggak perlu mengatur apa-apa.

---

Berikutnya: DNS, yang nerjemahin nama domain jadi IP address.
