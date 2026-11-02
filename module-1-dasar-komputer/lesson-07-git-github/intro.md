## Kenapa Perlu Git

Pernah punya folder tugas yang isinya begini?

```
laporan.docx
laporan-revisi.docx
laporan-revisi-final.docx
laporan-revisi-final-fix.docx
laporan-revisi-final-fix-beneran.docx
```

Semua orang pernah. Masalahnya, dua minggu kemudian lu nggak tahu lagi mana yang terbaru, dan apa bedanya antara satu file dengan file lainnya.

Di coding masalahnya lebih parah, karena satu proyek isinya puluhan file yang saling bergantung. Lu ubah tiga file, program tiba-tiba error, dan lu nggak ingat apa yang barusan diubah.

### Git menyelesaikan itu

Git nyimpen riwayat perubahan di satu folder yang sama. Lu nggak perlu bikin salinan file. Tiap kali lu merasa kondisi kodenya layak disimpan, lu bikin satu catatan yang namanya **commit**.

Analoginya buku catatan kasbon di warung. Tiap transaksi dicatat: tanggal, siapa, berapa. Kalau ada yang bingung soal utang bulan lalu, tinggal buka catatannya dan lihat urutan kejadiannya. Commit itu satu baris di buku kasbon itu, tapi untuk kode.

### Git dan GitHub itu beda

- **Git** adalah program di laptop lu. Dia yang nyimpen riwayat.
- **GitHub** adalah website tempat nyimpen salinan proyek Git secara online. Fungsinya mirip Google Drive, tapi khusus untuk proyek kode.

Lu bisa pakai Git tanpa GitHub. Kebalikannya nggak bisa.

### Yang Bakal Lu Bisa Setelah Lesson Ini

- Bikin repository baru dan menyimpan perubahan lewat commit
- Melihat riwayat dan apa saja yang berubah
- Membatalkan perubahan yang belum disimpan, dan mengembalikan commit lama
- Mencoba perubahan di branch tanpa mengganggu versi utama
- Mengirim proyek lu ke GitHub

### Istilah yang Dipakai

Tiga istilah ini bakal sering muncul. Jangan dihafal sekarang, nanti juga kebiasa.

| Istilah | Artinya |
|---|---|
| Repository (repo) | Folder proyek yang sudah dipantau Git |
| Commit | Satu catatan perubahan yang tersimpan, lengkap dengan pesan |
| Branch | Jalur terpisah buat nyoba perubahan tanpa ngerusak versi utama |

Buka terminal lu, kita mulai.
