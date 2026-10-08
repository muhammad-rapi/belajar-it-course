## Exercises - Internet & Web

Praktek DNS lookup, HTTP request, dan traceroute.

---

### Exercise 1: DNS Lookup

**Tujuan**: Cari IP address dari domain.

**Commands**:
```bash
# Lookup google.com
nslookup google.com

# Atau pake dig (more detail)
dig google.com

# Atau host
host google.com
```

**Expected Output** (nslookup):
```
Server:  8.8.8.8
Name:    google.com
Address: 142.250.185.46
```

**Task tambahan**: Lookup IP dari:
- facebook.com
- twitter.com
- github.com

---

### Exercise 2: HTTP Request dengan curl

**Tujuan**: Kirim HTTP request manual.

**GET request simple**:
```bash
curl https://jsonplaceholder.typicode.com/users/1
```

**Expected Output**: JSON data user

**Dengan headers**:
```bash
curl -I https://google.com
```

Output: Response headers (status code, content-type, dll)

**POST request**:
```bash
curl -X POST https://jsonplaceholder.typicode.com/posts \
  -H "Content-Type: application/json" \
  -d '{"title": "Test", "body": "Hello", "userId": 1}'
```

---

### Exercise 3: Traceroute

**Tujuan**: Liat route ke server.

**macOS/Linux**:
```bash
traceroute google.com
```

**Windows**:
```bash
tracert google.com
```

**Expected Output**:
```
1  192.168.1.1  2ms  (router rumah)
2  10.0.0.1     5ms  (ISP)
...
15 142.250.185.46  20ms (google.com)
```

**Analisa**: Berapa hop (lompatan)? Latency berapa?

---

## Checklist

- [ ] Lu bisa lookup IP dari domain
- [ ] Lu bisa kirim HTTP request pake curl
- [ ] Lu paham traceroute output
- [ ] Lu ngerti status code (200, 404, 500)

---

Next: **Summary** - ringkasan Internet & Web.
