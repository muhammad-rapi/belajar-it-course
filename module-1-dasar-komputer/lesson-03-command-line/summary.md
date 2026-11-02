## Summary

**Yang udah lu pelajari**

- Terminal adalah antarmuka teks buat ngasih perintah. Cocok buat kerjaan berulang, tools developer, dan server.
- Bagian sebuah perintah: nama perintah, opsi, dan argumen.
- Sepuluh perintah dasar:

| Perintah | Fungsi | Contoh |
|---|---|---|
| `pwd` | lihat posisi sekarang | `pwd` |
| `ls` | lihat isi folder | `ls -la` |
| `cd` | pindah folder | `cd Documents` |
| `mkdir` | bikin folder | `mkdir project` |
| `touch` | bikin file kosong | `touch app.py` |
| `rm` | hapus | `rm file.txt` |
| `cp` | salin | `cp a.txt b.txt` |
| `mv` | pindah atau ganti nama | `mv old.txt new.txt` |
| `cat` | lihat isi file | `cat file.txt` |
| `clear` | bersihkan layar | `clear` |

- Path absolut dimulai dari root. Path relatif dihitung dari posisi sekarang. Simbolnya `.`, `..`, dan `~`.
- `rm` menghapus permanen. Cek dulu dengan `ls`.

**Kenapa ini kepakai nanti**

Semua yang berikut dijalankan di terminal:

```bash
python3 app.py
npm install
git add .
git commit -m "pesan"
```

**Cek sebelum lanjut**

- Lu bisa buka terminal tanpa bingung.
- Lu bisa pindah folder pakai `cd`, termasuk path relatif.
- Lu paham kenapa `rm` perlu hati-hati.

## Tips Biar Makin Lancar

- Pakai terminal buat kerjaan kecil, misalnya bikin folder atau lihat isi folder, supaya cepat terbiasa.
- Pakai `Tab` buat melengkapi nama, dan tombol panah atas buat mengulang perintah.
- Pintasan yang berguna: `Ctrl + A` (ke awal baris), `Ctrl + E` (ke akhir baris), `Ctrl + R` (cari perintah lama).
- Untuk belajar lebih jauh: [Command Line Crash Course (MDN)](https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Environment_setup/Command_line) dan [cmdchallenge.com](https://cmdchallenge.com/).

## Lanjut Kemana?

Di Lesson 4, lu belajar gimana data bergerak lewat internet: IP, HTTP, dan DNS. Beberapa perintah terminal yang barusan lu pelajari dipakai di sana buat ngecek koneksi dan mengirim permintaan.
