## Summary

**Yang udah lu pelajari**

- **Internet** adalah jaringan dari jaringan. **Web** adalah salah satu layanan di atasnya.
- **IP address** adalah alamat tiap perangkat. **Router** mengarahkan paket ke tujuan.
- Data dikirim sebagai **paket** kecil yang digabung lagi di tujuan.
- **Client** meminta, **server** membalas. Polanya disebut permintaan dan balasan.
- **HTTP** punya method: GET (ambil), POST (bikin), PUT (ganti), PATCH (ubah sebagian), DELETE (hapus).
- **Status code**: 2xx berhasil, 3xx dialihkan, 4xx masalah di permintaan, 5xx masalah di server.
- **HTTPS** mengenkripsi data, HTTP nggak.
- **DNS** nerjemahin nama domain jadi IP address, dengan cache di tiap tahap. Perubahan DNS butuh waktu buat menyebar.

**Perintah yang dipakai**

```bash
nslookup github.com
curl https://example.com
curl -I https://example.com
traceroute google.com
```

**Cek sebelum lanjut**

- Lu bisa bedain 200, 404, dan 500.
- Lu bisa jelasin apa yang terjadi saat mengetik alamat web.
- Lu bisa pakai `nslookup` dan `curl`.

## Lanjut Kemana?

Di Lesson 5, lu lihat bagian setelah balasan sampai: gimana browser mengolah HTML, CSS, dan JavaScript jadi halaman, dan gimana ngintip semua itu lewat DevTools.
