## Kesalahan Umum

### 1. `command not found`

```
bash: cdd: command not found
```

Penyebab paling sering: salah ketik nama perintah. Cek ejaannya. Kalau perintahnya memang benar tapi tetap nggak dikenali, kemungkinan program itu belum terpasang atau terminal belum dibuka ulang setelah instalasi.

### 2. `No such file or directory`

```
cd: no such file or directory: Dokumen
```

Foldernya nggak ada di posisi lu sekarang. Jalankan `ls` buat lihat nama yang benar. Di macOS dan Linux, huruf besar dan kecil dibedakan, jadi `documents` dan `Documents` itu dua nama berbeda. Pakai `Tab` buat melengkapi nama otomatis, supaya nggak salah ketik.

### 3. Nggak tahu lagi ada di folder mana

Gejalanya: file yang lu bikin nggak ketemu, atau `cd` nggak jalan seperti dugaan. Jalankan `pwd` buat lihat posisi. Kalau bingung, `cd ~` selalu bawa lu balik ke home.

### 4. Spasi di nama folder

```bash
cd Belajar Python
```

Terminal baca spasi sebagai pemisah, jadi `Belajar` dan `Python` dianggap dua hal berbeda. Bungkus dengan tanda kutip (`cd "Belajar Python"`) atau, lebih baik lagi, bikin nama tanpa spasi (`belajar-python`).

### 5. `rm` yang terlalu cepat

`rm` langsung menghapus, tanpa tanya dan tanpa Trash. Tiga kebiasaan yang aman:

- Jalankan `ls` dulu buat memastikan folder yang akan dihapus.
- Baca ulang perintah sebelum menekan Enter.
- Jangan pernah jalankan `rm -rf` dari tutorial yang lu nggak paham.

Terutama waspadai `rm -rf /` dan `rm -rf ~`. Dua perintah itu mencoba menghapus seluruh sistem atau seluruh folder home lu. Sistem modern sering menolak yang pertama, tapi jangan dicoba.

### 6. Menempel perintah dari internet tanpa dibaca

Terminal menjalankan apa pun yang lu tempel. Kalau lu nemu perintah di forum atau artikel, baca dulu tiap bagiannya. Kalau ada bagian yang nggak lu ngerti, cari tahu dulu. Hindari perintah yang diawali `sudo` kecuali dokumentasi resminya yang nyuruh.

### 7. Beda perintah di Windows

Perintah seperti `ls`, `touch`, dan `cat` nggak ada di Command Prompt (CMD) bawaan Windows. Pakai Git Bash atau PowerShell, atau lihat tabel padanan di bagian Perintah Dasar.
