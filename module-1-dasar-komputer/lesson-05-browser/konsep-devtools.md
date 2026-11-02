## DevTools: Peta Tab-nya

DevTools adalah panel yang nempel di browser dan nampilin isi halaman dari sisi teknis.

---

### Cara Buka

| Sistem | Buka DevTools | Langsung ke mode inspect |
|---|---|---|
| macOS | `Cmd + Option + I` | `Cmd + Option + C` |
| Windows / Linux | `F12` atau `Ctrl + Shift + I` | `Ctrl + Shift + C` |

Cara lain yang berlaku di semua sistem: klik kanan di bagian mana pun di halaman, lalu pilih **Inspect**.

Waktu pertama dibuka, panel biasanya muncul di bawah atau di kanan layar. Kalau terlalu sempit, klik ikon tiga titik di pojok panel dan pilih posisi dock yang lu suka. Gunakan "Undock into separate window" kalau lu punya dua monitor.

---

### Tab yang Paling Sering Dipakai

DevTools punya belasan tab. Buat pemula, tiga tab ini cukup buat 90 persen kebutuhan:

**Elements**: nampilin DOM dan CSS-nya. Dipakai buat ngecek struktur halaman dan ngoprek tampilan.

**Console**: tempat pesan error dan hasil `console.log()` muncul. Di sini lu juga bisa ngetik JavaScript langsung.

**Network**: daftar semua request yang dikirim halaman, lengkap dengan status dan response-nya.

---

### Tab Lain, Kenalan Aja Dulu

**Sources**: baca file JavaScript dan pasang breakpoint buat berhenti di baris tertentu. Baru kepakai waktu lu udah nulis JavaScript yang lumayan panjang.

**Application**: ngelihat cookies dan localStorage.

**Performance** dan **Lighthouse**: ngukur seberapa cepat halaman dimuat. Dipakai belakangan, waktu lu mulai ngoptimasi website.

Nggak usah dipaksa ngerti semuanya sekarang. Lu bakal nemu kebutuhan tiap tab satu per satu seiring jalan.

---

### Shortcut yang Layak Dihafal

- `Cmd + Shift + C` / `Ctrl + Shift + C`: pilih elemen langsung dari halaman
- `Cmd + R` / `Ctrl + R`: refresh halaman
- `Cmd + Shift + R` / `Ctrl + Shift + R`: refresh sambil ngabaikan cache. Berguna kalau perubahan lu nggak kelihatan padahal udah disimpan.
- `Cmd + K` / `Ctrl + L`: bersihin Console

---

### Device Toolbar

Di pojok kiri atas panel ada ikon HP dan tablet. Klik itu buat liat halaman dalam ukuran layar ponsel. Hampir semua website sekarang dibuka dari HP, jadi kebiasaan ngecek tampilan mobile ini penting dari awal.
