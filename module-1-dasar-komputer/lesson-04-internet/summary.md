## Summary - Internet & Web

Lu udah paham gimana data ngalir lewat internet.

---

## Key Concepts

**Internet**:
- Network of networks
- IP address = alamat unik tiap device
- Packet switching = data dipecah jadi packet kecil
- Router = forward packet ke tujuan

**HTTP**:
- Request-response protocol
- Methods: GET (ambil), POST (create), PUT (update), DELETE (hapus)
- Status codes: 2xx (success), 4xx (client error), 5xx (server error)
- HTTPS = encrypted (SSL/TLS)

**DNS**:
- Phonebook internet
- Translate domain → IP
- Cache di browser, OS, router
- Propagation: 24-48 jam

---

## Kenapa Ini Penting Buat Developer?

**Waktu bikin app**:
```python
import requests

# HTTP GET request
response = requests.get("https://api.example.com/users")
print(response.status_code)  # 200

if response.status_code == 200:
    data = response.json()
    print(data)
```

Lu harus paham:
- Request method (GET, POST, dll)
- Status code (200 = ok, 404 = not found)
- JSON response format

---

## Next Steps

**Next lesson: Browser & DevTools** - inspect web page, debug, console.

Preview:
- How browser works
- DevTools (inspect element, network tab, console)
- Debug JavaScript

Sebelum lanjut:
- [ ] Paham client-server model
- [ ] Hafal HTTP status codes umum (200, 404, 500)
- [ ] Bisa lookup DNS
- [ ] Comfortable pake curl

---

Ready buat Lesson 5! 🌐
