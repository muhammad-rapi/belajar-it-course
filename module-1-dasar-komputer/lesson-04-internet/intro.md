## Kenapa Perlu Paham Internet?

Lu pake internet tiap hari: browsing, streaming, chat. Tapi pernah mikir gimana cara kerjanya?

---

### Masalah Kalau Ga Ngerti

**1. Bingung waktu ada error**

```
ERR_CONNECTION_REFUSED
DNS_PROBE_FINISHED_NXDOMAIN
504 Gateway Timeout
```

Kalau ga ngerti internet, lu cuma bisa restart router. Ga tau masalahnya dimana.

**2. Ga bisa bikin app yang connect ke internet**

Semua app modern butuh internet:
- Chat app → send message ke server
- E-commerce → fetch product dari database
- Game → sync score ke cloud

Lu harus paham **request-response**, **API**, **HTTP methods**.

**3. Debugging susah**

```python
response = requests.get("https://api.example.com/data")
print(response.status_code)  # 404
```

Lu harus tau: 404 itu apa? Kenapa? Gimana fixnya?

---

### Analogi: Sistem Pos

> Lu mau kirim surat ke temen:
> 1. Tulis surat (data)
> 2. Masukin amplop, tulis alamat (IP address)
> 3. Kasih ke kantor pos (router)
> 4. Kantor pos deliver ke alamat tujuan
> 5. Temen baca surat, balas (response)
> 6. Balasan sampe ke lu

Internet works the same. Komputer lu = pengirim, server = penerima, router = kantor pos.

---

## Apa yang Lu Bakal Pelajari

- Apa itu Internet (vs WWW)
- IP Address & routing
- HTTP: request methods (GET, POST, PUT, DELETE)
- DNS: translate google.com → 142.250.185.46
- Client-server model
- Response codes (200, 404, 500)

---

Ready? Let's dive in.
