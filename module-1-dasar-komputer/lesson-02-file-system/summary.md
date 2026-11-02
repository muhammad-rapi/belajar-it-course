## Summary

**Yang udah lu pelajari**

- **Root** adalah titik awal file system. `C:\` di Windows, `/` di macOS dan Linux.
- **Path absolut** adalah alamat lengkap dari root. **Path relatif** adalah alamat dari posisi lu sekarang.
- Tiga simbol: `.` (folder ini), `..` (folder di atasnya), `~` (home).
- **Ekstensi** nentuin aplikasi yang membuka file, dan bisa dipakai buat nipu kalau tersembunyi.
- **Permissions** di macOS dan Linux: `r`, `w`, `x` buat owner, group, dan others.
- Pola umum: `644` buat file biasa, `755` buat folder dan script, `600` buat file rahasia.
- Spasi di nama file bikin repot di terminal. Pakai tanda hubung.

**Perintah yang dipakai di lesson ini**

```bash
ls -l file.txt          # lihat permissions
ls -a                   # lihat file tersembunyi
chmod 644 file.txt      # ubah permissions
chmod +x script.sh      # tambah izin jalankan
mkdir -p a/b/c          # bikin folder bertingkat
```

## Lanjut Kemana?

Di Lesson 3, lu mulai pindah-pindah folder dan bikin file lewat terminal. Semua yang barusan lu pelajari soal path langsung kepakai di sana.
