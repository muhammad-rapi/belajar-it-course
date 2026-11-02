## Komputer Itu Apa

![Setup komputer](https://images.unsplash.com/photo-1587831990711-23ca6441447b?w=800&q=80)
*Foto oleh [Kari Shea](https://unsplash.com/@karishea) di [Unsplash](https://unsplash.com)*

Komputer adalah mesin yang bisa menyimpan data, memproses data, dan menampilkan hasilnya dengan sangat cepat. Itu intinya.

### Analogi Dapur

Bayangin lu lagi masak nasi goreng:

- **Bahan (data)**: nasi, telur, bumbu. Ini yang mau diolah.
- **Kompor dan wajan (CPU)**: alat buat ngolah bahan.
- **Kulkas (storage)**: tempat nyimpen bahan buat jangka panjang.
- **Meja kerja (RAM)**: tempat naruh bahan yang lagi dipakai sekarang.
- **Piring (output)**: hasil masakan yang siap disajikan, yaitu tampilan di layar.
- **Resep (software)**: instruksi cara masaknya.
- **Pengatur dapur (sistem operasi)**: yang ngambil bahan dari kulkas, naruh di meja, dan nyalain kompor pada waktu yang pas.

Komputer kerja persis begitu, cuma jauh lebih cepat. Dia bisa ngerjain miliaran langkah dalam satu detik.

```mermaid
graph TD
    A[Pengatur dapur<br/>Operating System] --> B[Kompor<br/>CPU]
    A --> C[Meja kerja<br/>RAM]
    A --> D[Kulkas<br/>Storage]

    B --> E[Piring<br/>Output]
    C -.Bahan sementara.-> B
    D -.Bahan permanen.-> C

    F[Resep<br/>Software] -.Instruksi.-> A

    style A fill:#fff3e0
    style B fill:#ffebee
    style C fill:#e3f2fd
    style D fill:#e8f5e9
    style E fill:#f3e5f5
    style F fill:#fce4ec
```
*Diagram: komponen komputer dengan analogi dapur*

<figure><img src="../../../assets/videos/kitchen-analogy.gif" alt="Animasi analogi dapur" width="100%"><figcaption><em>CPU, RAM, dan storage dijelasin lewat analogi dapur</em></figcaption></figure>

Coba perhatikan: kalau lu hapus salah satu bagian, dapurnya nggak bisa jalan. Kompor tanpa bahan nggak ada gunanya. Bahan tanpa resep nggak jadi apa-apa.
