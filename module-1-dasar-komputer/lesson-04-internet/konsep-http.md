## HTTP - HyperText Transfer Protocol

HTTP = **protocol buat web browsing**. Cara browser minta data dari server.

---

### Request-Response Cycle

**1. Client (browser) kirim request**

```
GET /search?q=python HTTP/1.1
Host: google.com
```

**2. Server proses & kirim response**

```
HTTP/1.1 200 OK
Content-Type: text/html

<html>
  <body>Hasil search...</body>
</html>
```

---

### HTTP Methods

**GET** = ambil data (ga ubah apa-apa di server)

```
GET /api/users/123
```

→ "Kasih data user ID 123"

**POST** = kirim data baru (create)

```
POST /api/users
Body: {"name": "Rafi", "email": "rafi@gmail.com"}
```

→ "Bikin user baru dengan data ini"

**PUT** = update data (ganti semua)

```
PUT /api/users/123
Body: {"name": "Rafi Updated", "email": "new@gmail.com"}
```

**DELETE** = hapus data

```
DELETE /api/users/123
```

**PATCH** = update sebagian data

```
PATCH /api/users/123
Body: {"email": "new@gmail.com"}  # Cuma ganti email
```

---

### HTTP Status Codes

Server kasih status code buat info request berhasil/gagal.

**2xx = Success**
- `200 OK` = Sukses
- `201 Created` = Data baru dibuat (after POST)

**3xx = Redirect**
- `301 Moved Permanently` = URL pindah permanent
- `302 Found` = Temporary redirect

**4xx = Client Error (salah lu)**
- `400 Bad Request` = Request salah format
- `401 Unauthorized` = Belum login
- `403 Forbidden` = Login tapi ga punya akses
- `404 Not Found` = URL ga ada
- `429 Too Many Requests` = Spam request, kena limit

**5xx = Server Error (salah server)**
- `500 Internal Server Error` = Server crash
- `502 Bad Gateway` = Gateway/proxy error
- `503 Service Unavailable` = Server down/maintenance
- `504 Gateway Timeout` = Server terlalu lama respond

---

### HTTPS (Secure)

**HTTP** = plain text (bisa disadap)  
**HTTPS** = encrypted (SSL/TLS)

**Perbedaan**:

```
HTTP:  google.com   → Data plain text
HTTPS: google.com   → Data encrypted 🔒
```

**Kenapa penting?**
- Login form → password ga bisa disadap
- Payment → credit card number aman
- Privacy → ISP ga bisa baca isi data

**Cara cek**: Browser ada icon gembok 🔒 kalau HTTPS.

---

### Headers

Request & response punya **headers** (metadata).

**Request headers**:
```
GET /api/data HTTP/1.1
Host: api.example.com
User-Agent: Mozilla/5.0
Authorization: Bearer token123
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

### Contoh Real: API Call

**Ambil data user** (GET):

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

**Bikin post baru** (POST):

```bash
curl -X POST https://jsonplaceholder.typicode.com/posts \
  -H "Content-Type: application/json" \
  -d '{"title": "Hello", "body": "World", "userId": 1}'
```

Response:
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

**HTTP/1.1** (old):
- 1 request per connection
- Slow

**HTTP/2** (modern):
- Multiple requests parallel
- Faster
- Most servers support sekarang

**HTTP/3** (newest):
- Based on QUIC (UDP instead of TCP)
- Faster lagi, especially on mobile

Browser otomatis pake yang terbaru. Lu ga perlu mikir.

---

Next: **DNS** - translate domain jadi IP.
