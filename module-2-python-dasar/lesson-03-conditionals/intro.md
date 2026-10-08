## Kenapa Perlu Conditionals?

Sampe sekarang, program lu jalan dari atas ke bawah, baris per baris. Semua code dijalanin. Ga ada pilihan.

**Masalahnya**: Real-world program perlu **bikin keputusan** berdasarkan kondisi.

---

### Skenario Real

**1. Login system**
```
Kalau password bener → login sukses
Kalau password salah → error, coba lagi
```

**2. Harga tiket bioskop**
```
Kalau umur < 12 → harga anak (30k)
Kalau umur 12-60 → harga normal (50k)
Kalau umur > 60 → harga senior (35k)
```

**3. ATM**
```
Kalau saldo >= jumlah tarik → transaksi sukses
Kalau saldo < jumlah tarik → saldo tidak cukup
```

Semua ini butuh **conditionals** - code yang jalan **cuma kalau kondisi tertentu terpenuhi**.

---

## Analogi: Lampu Lalu Lintas

Bayangin lu nyetir mobil:

```
Kalau lampu HIJAU → jalan
Kalau lampu MERAH → berhenti
Kalau lampu KUNING → hati-hati
```

Lu ga bisa jalan terus tanpa liat lampu. Lu harus **cek kondisi** (warna lampu) → **baru ambil keputusan** (jalan/berhenti).

Programming sama persis.

---

## Apa yang Lu Bakal Pelajari

Abis lesson ini, lu bisa:
- Bikin program yang "mikir" berdasarkan kondisi
- Paham operator perbandingan (`==`, `>`, `<`, dll)
- Pakai logic operators (`and`, `or`, `not`)
- Handle multiple kondisi (if-elif-else)
- Bikin simple decision-making program (quiz, kalkulator grading, dll)

---

## Preview Code

**Contoh simple**:

```python
umur = 17

if umur >= 18:
    print("Boleh masuk")
else:
    print("Belum cukup umur")
```

Output: `Belum cukup umur`

**Contoh dengan multiple kondisi**:

```python
nilai = 85

if nilai >= 90:
    print("Grade: A")
elif nilai >= 80:
    print("Grade: B")
elif nilai >= 70:
    print("Grade: C")
else:
    print("Grade: D")
```

Output: `Grade: B`

---

Ready? Mulai dari **If Statement** dasar.
