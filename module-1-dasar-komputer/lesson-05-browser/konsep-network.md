## Network Tab: Ngintip Request

Di Lesson 4 lu belajar HTTP lewat teks. Di tab Network lu bisa liat HTTP itu langsung terjadi.

---

### Cara Pakai

1. Buka DevTools, pilih tab **Network**.
2. Refresh halaman (`Cmd + R` / `Ctrl + R`). Kalau tab Network dibuka setelah halaman selesai dimuat, daftarnya kosong.
3. Satu per satu request muncul. Satu halaman biasa bisa ngirim puluhan sampai ratusan request: HTML, CSS, JavaScript, gambar, font, dan data API.

---

### Membaca Daftar Request

Kolom yang penting:

- **Name**: nama file atau alamat yang diminta
- **Status**: kode hasil dari server
- **Type**: jenis isinya (document, stylesheet, script, png, fetch)
- **Size**: ukuran data yang diterima
- **Time**: lama waktu dari request sampai response selesai

Status code yang udah lu kenal dari Lesson 4 muncul di sini:

- `200`: berhasil
- `301` / `302`: dialihkan ke alamat lain
- `404`: nggak ditemukan. Biasanya salah alamat file atau URL API.
- `500`: server error. Masalahnya ada di sisi server, bukan di komputer lu.

Baris dengan status gagal ditandai warna merah, jadi gampang ketahuan.

---

### Klik Satu Request

Klik salah satu baris, lalu liat panel yang muncul di sebelahnya:

- **Headers**: alamat yang diminta, method (GET, POST, dll), dan header yang dikirim dan diterima
- **Preview** / **Response**: isi balasan dari server. Kalau itu API, biasanya berupa JSON.
- **Timing**: rincian waktu, misalnya berapa lama nunggu server dan berapa lama download

Waktu lu debug API, ini tempat pertama yang dicek. Kirim request berhasil atau nggak? Status-nya berapa? Server balas apa? Tiga pertanyaan itu bisa dijawab dari tab ini.

---

### Memfilter Request

Di atas daftar ada tombol filter: **Fetch/XHR**, **JS**, **CSS**, **Img**, dan lainnya. Pilih **Fetch/XHR** buat nampilin cuma request data (API), tanpa gambar dan file CSS yang bikin ramai.

---

### Menemukan Halaman yang Lambat

Urutkan kolom **Time** dari yang terbesar. Request paling lama biasanya jadi penyebab halaman terasa berat. Penyebab umum yang bakal lu temuin:

- gambar yang ukurannya jauh lebih besar dari yang dibutuhkan
- file JavaScript yang terlalu gede
- request ke server yang jauh atau lambat

Ada juga dropdown **No throttling**. Ganti ke **Slow 4G** buat nyimulasiin koneksi lambat. Ini ngebantu lu ngerasain gimana website lu di HP dengan sinyal jelek.
