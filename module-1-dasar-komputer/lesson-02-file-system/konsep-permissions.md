## Permissions

**Permissions** adalah aturan siapa yang boleh membaca, mengubah, atau menjalankan sebuah file atau folder.

Bayangin kamar kos. Lu sebagai pemilik boleh masuk, tidur, dan ngatur isinya. Temen deket boleh masuk dan duduk, tapi nggak boleh mindahin kasur. Orang asing nggak boleh masuk sama sekali. File di komputer punya aturan yang mirip.

---

### Di Windows

Windows pakai **atribut** yang lebih sederhana:

- **Read-only**: file cuma bisa dibaca, nggak bisa diubah
- **Hidden**: file disembunyikan dari tampilan biasa

Buat ngeceknya, klik kanan file, pilih **Properties**, lalu lihat bagian **Attributes** di tab General.

---

### Di macOS dan Linux

Sistemnya lebih rinci. Ada tiga jenis izin:

| Izin | Huruf | Artinya |
|---|---|---|
| Read | `r` | boleh membaca isi file |
| Write | `w` | boleh mengubah atau menghapus file |
| Execute | `x` | boleh menjalankan file (kalau itu program atau script) |

Dan tiga kelompok pengguna:

| Kelompok | Siapa |
|---|---|
| Owner | pemilik file |
| Group | grup yang ditetapkan ke file |
| Others | semua orang selain itu |

Hasilnya ditulis sebagai sembilan karakter, tiga untuk tiap kelompok:

```
rwx  r-x  r--
│││  │││  │││
│││  │││  └└└─ Others: baca saja
│││  └└└─────── Group: baca dan jalankan
└└└──────────── Owner: baca, ubah, dan jalankan
```

Tanda `-` artinya izin itu nggak ada.

**Cara melihat**

```bash
ls -l file.txt
```

Hasilnya seperti ini (angka dan nama di tiap komputer beda):

```
-rw-r--r--  1 rafi  staff  1234 Oct  7 10:00 file.txt
```

Sembilan karakter setelah tanda `-` pertama (`rw-r--r--`) adalah permissions-nya. Artinya: owner boleh baca dan ubah, group dan others cuma boleh baca.

**Cara mengubah dengan angka**

Tiap izin punya nilai: `r` = 4, `w` = 2, `x` = 1. Jumlahkan per kelompok.

| Angka | Izin | Artinya |
|---|---|---|
| 7 | rwx | 4 + 2 + 1 |
| 6 | rw- | 4 + 2 |
| 5 | r-x | 4 + 1 |
| 4 | r-- | 4 |

Tiga angka berurutan adalah owner, group, others:

```bash
chmod 644 file.txt    # owner baca dan ubah, lainnya baca saja
chmod 755 script.sh   # owner semua, lainnya baca dan jalankan
chmod 600 rahasia.txt # hanya owner yang boleh baca dan ubah
```

Cara lain yang lebih singkat buat nambah izin jalankan:

```bash
chmod +x script.sh
```

---

### Prinsip yang Layak Diingat

**Kasih izin seperlunya.** `chmod 777` artinya semua orang boleh baca, ubah, dan jalankan. Itu jarang dibutuhkan, dan membuka peluang file lu diubah oleh program atau pengguna lain.

Pola yang aman buat awal:

- File biasa: `644`
- Folder dan script yang dijalankan: `755`
- File yang berisi rahasia, misalnya kunci SSH: `600`
