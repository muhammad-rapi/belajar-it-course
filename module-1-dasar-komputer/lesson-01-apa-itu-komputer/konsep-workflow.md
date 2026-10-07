### Putting It All Together: Workflow Komputer

**Scenario**: Kamu buka Chrome, ketik "google.com", enter.

**What happens** (simplified):

1. **Input**: Kamu ketik di keyboard → OS detect keystroke → pass ke Chrome.
2. **Process**:
   - Chrome (app) minta OS: "Gue butuh RAM 500 MB buat load page ini."
   - OS alokasi RAM dari pool available.
   - Chrome kirim HTTP request ke google.com (via network card).
   - Google server bales dengan HTML/CSS/JS.
3. **CPU works**:
   - Parse HTML (CPU baca struktur page).
   - Render CSS (hitung layout, warna, font).
   - Execute JavaScript (animasi, interaktif).
4. **GPU works** (kalau ada):
   - Render visual (gambar, video) ke pixel.
5. **Output**: Monitor nampilin Google homepage.

**Total time**: <1 detik (miliaran instruksi dieksekusi).

<!-- DIAGRAM: Computer Workflow -->
```mermaid
graph LR
    A[Input<br/>Keyboard] --> B[CPU<br/>Process]
    B --> C[RAM<br/>Working Memory]
    C --> D[Network<br/>HTTP Request]
    D --> E[Server<br/>Google]
    E --> D
    D --> B
    B --> F[Output<br/>Monitor Display]
    
    style A fill:#e3f2fd
    style B fill:#fff3e0
    style C fill:#f3e5f5
    style D fill:#e8f5e9
    style E fill:#fce4ec
    style F fill:#e3f2fd
```
*Diagram: Computer workflow ketika buka google.com*

**📹 Video Explanation:**

<figure><img src="../../../assets/videos/computer-workflow.gif" alt="Computer Workflow Animation" width="100%"><figcaption><em>Input → Process → Network → Output dalam 25 detik</em></figcaption></figure>

**Coba perhatikan**:
- Semua ini happen **otomatis**. OS + Chrome handle complexity. Kamu cuma "ketik + enter".
- Ini kenapa **faster hardware = better experience**. CPU/RAM/SSD lebih cepat = workflow ini lebih cepat.

---