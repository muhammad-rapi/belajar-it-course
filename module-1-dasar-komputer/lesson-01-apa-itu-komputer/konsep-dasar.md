### Komputer itu Apa Sih?

![Modern Computer Setup](https://images.unsplash.com/photo-1587831990711-23ca6441447b?w=800&q=80)
*Photo by [Kari Shea](https://unsplash.com/@karishea) on [Unsplash](https://unsplash.com)*

**Definisi simple**: Komputer itu mesin yang bisa **nyimpen data**, **proses data**, dan **nampilin hasil** dengan cepat. Segitu doang.

**Analogi: Dapur**

> Bayangin kamu masak nasi goreng:
> - **Bahan (data)**: nasi, telur, bumbu (ini data yang mau diproses)
> - **Kompor + wajan (processor)**: alat buat masak (process data)
> - **Kulkas (storage)**: tempat simpen bahan (long-term storage)
> - **Meja kerja (RAM)**: tempat naruh bahan yang lagi dipake (short-term, working memory)
> - **Piring (output)**: hasil masakan yang siap disajikan (display/print)
> - **Resep (software)**: instruksi cara masaknya (program/code)
> - **Kamu (operating system)**: yang koordinasi semua (ambil bahan dari kulkas, taruh di meja, nyalain kompor, dll)

Komputer kerja persis kayak gini, cuma jauh lebih cepat (milyaran operasi per detik).

<!-- DIAGRAM: Kitchen Analogy -->
```mermaid
graph TD
    A[Kamu<br/>Operating System] --> B[Kompor<br/>CPU]
    A --> C[Meja Kerja<br/>RAM]
    A --> D[Kulkas<br/>Storage]
    
    B --> E[Piring<br/>Output]
    C -.Bahan Sementara.-> B
    D -.Bahan Permanen.-> C
    
    F[Resep<br/>Software] -.Instruksi.-> A
    
    style A fill:#fff3e0
    style B fill:#ffebee
    style C fill:#e3f2fd
    style D fill:#e8f5e9
    style E fill:#f3e5f5
    style F fill:#fce4ec
```
*Diagram: Analogi dapur - gimana komponen komputer kerja bareng*

**📹 Video Explanation:**

<figure><img src="../../../assets/videos/kitchen-analogy.gif" alt="Kitchen Analogy Animation" width="100%"><figcaption><em>CPU, RAM, dan Storage explained dengan analogi dapur</em></figcaption></figure>

---