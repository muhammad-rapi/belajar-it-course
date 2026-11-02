## Workflow: Dari Ketik Sampai Muncul di Layar

Kita gabungin semuanya lewat satu contoh: lu buka Chrome, ketik `google.com`, lalu tekan Enter.

### Urutan Kejadiannya (Disederhanakan)

1. **Input**: lu ngetik di keyboard. OS mendeteksi tombol yang ditekan dan meneruskannya ke Chrome.
2. **Chrome minta sumber daya**: Chrome bilang ke OS, "Aku butuh RAM buat nampung halaman ini." OS ngasih jatah RAM.
3. **Ambil data**: Chrome kirim permintaan lewat jaringan ke server Google. Server balas dengan HTML, CSS, dan JavaScript.
4. **CPU kerja**: CPU baca struktur halaman, ngitung tata letak, dan ngejalanin JavaScript.
5. **GPU kerja** (kalau ada): gambar dan video diubah jadi piksel buat ditampilkan.
6. **Output**: monitor nampilin halaman Google.

Semua itu biasanya selesai dalam hitungan detik, atau kurang.

```mermaid
graph LR
    A[Input<br/>Keyboard] --> B[CPU<br/>Proses]
    B --> C[RAM<br/>Memori kerja]
    C --> D[Jaringan<br/>Permintaan HTTP]
    D --> E[Server<br/>Google]
    E --> D
    D --> B
    B --> F[Output<br/>Monitor]

    style A fill:#e3f2fd
    style B fill:#fff3e0
    style C fill:#f3e5f5
    style D fill:#e8f5e9
    style E fill:#fce4ec
    style F fill:#e3f2fd
```
*Diagram: alur komputer saat lu buka google.com*

<figure><img src="../../../assets/videos/computer-workflow.gif" alt="Animasi alur kerja komputer" width="100%"><figcaption><em>Input, proses, jaringan, lalu output</em></figcaption></figure>

### Coba Perhatikan

- Semua langkah ini jalan otomatis. Lu cuma ngetik dan tekan Enter.
- Hardware yang lebih cepat bikin tiap langkahnya lebih cepat, dan itu yang lu rasain sebagai komputer yang "ngebut".
- Langkah ke-3 (jaringan) dibahas lebih dalam di Lesson 4, dan langkah ke-4 (browser mengolah halaman) di Lesson 5.
