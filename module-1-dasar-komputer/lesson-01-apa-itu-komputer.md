# Apa itu Komputer? (Yang Sering Dilupain)

## Masalah yang Akan Kita Selesaikan

Kamu pasti udah pake komputer/laptop berkali-kali. Buka Chrome, ngetik dokumen, download file, install aplikasi. Tapi pernah mikir gimana cara kerjanya?

Kebanyakan orang langsung loncat ke "belajar coding" tanpa ngerti dasar-dasar komputer. Ujungnya bingung waktu ada error kayak "memory full", "CPU 100%", atau "app not responding". Ga ngerti kenapa bisa begitu, gimana cara fixnya.

Lesson ini bakal jelasin **apa yang terjadi di balik layar** waktu kamu pake komputer. Ga perlu jadi teknisi, tapi kamu harus ngerti konsep dasar: hardware, software, operating system, dan gimana mereka collaborate.

Setelah lesson ini, kamu bakal punya mental model yang clear tentang komputer. Waktu belajar programming nanti, kamu ga cuma "ikutin tutorial" tapi **paham kenapa code kamu jalan** (atau kenapa ga jalan).

## Konsep Utama

### Komputer itu Apa Sih?

**Definisi simple**: Komputer itu mesin yang bisa **nyimpen data**, **proses data**, dan **nampilin hasil** dengan cepat. That's it.

**Analogi: Dapur**

> Bayangin kamu masak nasi goreng:
> - **Bahan (data)**: nasi, telur, bumbu (ini data yang mau diproses)
> - **Kompor + wajan (processor)**: alat buat masak (process data)
> - **Kulkas (storage)**: tempat simpen bahan (long-term storage)
> - **Meja kerja (RAM)**: tempat naruh bahan yang lagi dipake (short-term, working memory)
> - **Piring (output)**: hasil masakan yang siap disajikan (display/print)
> - **Resep (software)**: instruksi cara masaknya (program/code)
> - **Kamu (operating system)**: yang koordinasi semua (ambil bahan dari kulkas, taruh di meja, nyalain kompor, dll)

Komputer works exactly like this, tapi jauh lebih cepat (milyaran operasi per detik).

---

### Hardware: Bagian Fisik Komputer

Hardware itu **semua yang bisa kamu sentuh**. Komponen fisik.

#### 1. CPU (Central Processing Unit) - Otak Komputer

**Fungsi**: Eksekusi instruksi (hitung, proses, decision).

**Analogi**: Koki yang masak. Semua proses masak (motong, tumis, aduk) dilakuin sama koki. Semakin jago kokinya (CPU cepat), semakin cepat masakannya selesai.

**Spec yang sering kamu lihat**:
- **Clock Speed** (GHz): Seberapa cepat CPU kerja. Contoh: 2.5 GHz = 2.5 milyar cycle per detik.
- **Cores**: Jumlah "koki". Dual-core = 2 koki (bisa masak 2 hal sekaligus). Quad-core = 4 koki.

**Real example**:
- Intel i3, i5, i7, i9 (angka lebih tinggi = lebih powerful)
- AMD Ryzen 3, 5, 7, 9
- Apple M1, M2, M3 (chip ARM, efficient)

**Kapan CPU penting**:
- Coding (compile code)
- Video editing
- Gaming
- Running heavy apps

**Coba perhatikan**:
- Waktu kamu buka banyak tab Chrome terus laptop ngelag? Itu CPU overload (terlalu banyak instruksi yang harus diproses sekaligus).
- Check CPU usage: Windows (Task Manager), Mac (Activity Monitor).

---

#### 2. RAM (Random Access Memory) - Meja Kerja

**Fungsi**: Simpen data **sementara** yang lagi dipake. Cepat diakses, tapi ilang kalau komputer dimatiin.

**Analogi**: Meja kerja kamu waktu masak. Kamu taruh bahan-bahan yang lagi dipake di meja (nasi, telur, bumbu) biar gampang diambil. Kalau mejanya kecil (RAM dikit), kamu harus bolak-balik ke kulkas tiap mau ambil bahan (lambat). Kalau mejanya lega (RAM banyak), semua bahan ada di meja (cepat).

**Spec yang sering kamu lihat**:
- **Capacity**: 4GB, 8GB, 16GB, 32GB. Lebih banyak = bisa buka lebih banyak apps sekaligus.
- **Speed**: DDR4, DDR5 (ga terlalu penting buat user biasa).

**Real example**:
- **4GB RAM**: Cukup buat browsing ringan, office apps. Tapi struggle kalau buka 20 tab Chrome.
- **8GB RAM**: Sweet spot buat user biasa (browsing, Netflix, coding ringan).
- **16GB+**: Buat developer (run Docker, VM), video editor, multitasker berat.

**Kapan RAM penting**:
- Multitasking (banyak apps buka sekaligus)
- Coding (IDE + browser + terminal + database)
- Photo/video editing
- Gaming

**Coba perhatikan**:
- Waktu RAM full, komputer jadi super lambat (disk swapping: pakai storage sebagai "RAM cadangan", tapi storage jauh lebih lambat).
- Check RAM usage: Task Manager (Windows) atau Activity Monitor (Mac).

---

#### 3. Storage - Kulkas/Gudang

**Fungsi**: Simpen data **permanen**. File, foto, video, aplikasi. Ga ilang waktu komputer dimatiin.

**Analogi**: Kulkas atau gudang. Kamu simpen bahan makanan di kulkas. Kapanpun kamu mau masak, ambil dari kulkas. Bedanya sama meja kerja (RAM): kulkas lebih lambat diakses, tapi bisa simpen lebih banyak dan ga ilang waktu listrik mati.

**Jenis storage**:

**HDD (Hard Disk Drive)** - Piringan putar:
- ✅ **Murah**: 1 TB cuma 400-600rb
- ✅ **Kapasitas besar**: 1 TB, 2 TB, 4 TB
- ❌ **Lambat**: 100 MB/s read speed
- ❌ **Ada bagian gerak**: bisa rusak kalau kejatuh

**SSD (Solid State Drive)** - Chip elektronik:
- ✅ **Cepat**: 500 MB/s (SATA) atau 3,000 MB/s (NVMe)
- ✅ **Ga ada bagian gerak**: lebih tahan banting
- ❌ **Lebih mahal**: 1 TB SSD ~1-1.5 juta

**Real example**:
- Laptop lama (HDD): Boot Windows 2-3 menit, buka app lambat.
- Laptop baru (SSD): Boot Windows 10-15 detik, buka app instant.

**Impact nyata**:
- Upgrade dari HDD ke SSD = **laptop kerasa 3x lebih cepat** (ini upgrade paling worth it).

**Kapan storage penting**:
- Simpen banyak file (foto, video, project)
- Install banyak apps/games

---

#### 4. Output Devices - Cara Komputer "Ngomong" ke Kamu

**Monitor/Screen**: Nampilin visual (text, image, video).  
**Speaker**: Output audio.  
**Printer**: Output fisik (kertas).

**Analogi**: Piring tempat naruh hasil masakan. Kamu masak (CPU proses), hasil akhirnya ditaro di piring (monitor nampilin hasil).

---

#### 5. Input Devices - Cara Kamu "Ngomong" ke Komputer

**Keyboard**: Input text/command.  
**Mouse/Trackpad**: Navigate UI, click.  
**Microphone**: Input audio (voice command, recording).  
**Camera**: Input video (video call, foto).

**Analogi**: Kamu kasih instruksi ke komputer. Kayak kamu kasih tau koki (CPU) mau masak apa.

---

### Software: Instruksi yang Bikin Hardware Berguna

Hardware tanpa software = mesin mati. Software = **instruksi** yang ngasih tau hardware apa yang harus dilakuin.

**Analogi**: Kompor tanpa resep = ga bisa masak apa-apa. Kamu butuh **resep (software)** buat ngasih tau gimana cara masak.

#### Jenis Software:

**1. Operating System (OS)** - Koordinator utama:
- **Windows** (PC gaming, office)
- **macOS** (Apple ecosystem, creative work)
- **Linux** (developer, server, open-source)

OS ngatur semua: akses hardware (CPU, RAM, storage), manage apps, handle input/output.

**Analogi**: Kamu yang koordinasi dapur. Kamu yang ambil bahan dari kulkas (storage), taruh di meja kerja (RAM), kasih ke koki (CPU), dan atur timing semua masakan selesai bareng.

**2. Applications (Apps)** - Tools spesifik:
- **Browser** (Chrome, Firefox): Akses internet.
- **Text Editor** (Word, Google Docs): Nulis dokumen.
- **IDE** (VS Code, PyCharm): Coding.
- **Games** (Dota, Valorant): Entertainment.

Setiap app punya **instruksi spesifik** (code) yang bilang ke OS: "Gue butuh RAM sekian, akses storage ini, render pixel di monitor sini."

**3. Drivers** - Penerjemah hardware:
Driver itu software kecil yang **translate** instruksi OS ke bahasa hardware.

Contoh:
- **Printer driver**: OS bilang "print dokumen ini". Driver translate ke instruksi yang printer ngerti (format, warna, ukuran kertas).
- **GPU driver** (NVIDIA, AMD): Game bilang "render grafik ini". Driver translate ke instruksi GPU.

Kalau driver ga install atau outdated, hardware ga bisa dipake (printer ga detect, game lag, dll).

---

### Operating System (OS): The Boss

OS itu **software paling penting**. Tanpa OS, komputer cuma besi mati.

**Fungsi OS**:
1. **Manage hardware**: Alokasi RAM ke apps, schedule CPU tasks, akses storage.
2. **Provide interface**: GUI (Graphical User Interface) atau CLI (Command Line Interface) buat user interact dengan komputer.
3. **Run applications**: Kasih environment buat apps jalan.
4. **Security**: Manage permissions (app mana yang boleh akses camera, file, dll).

**Analogi: Manajer Restoran**

> OS itu manajer restoran. Dia koordinasi:
> - **Koki (CPU)**: Assign tugas masak apa, prioritas mana yang urgent.
> - **Meja kerja (RAM)**: Alokasi space buat tiap pesanan.
> - **Gudang (storage)**: Manage inventory bahan.
> - **Pelayan (I/O)**: Terima order dari customer (input), antar makanan (output).
> - **Kasir (security)**: Cek payment, manage akses.

**Real example**:

**Windows**:
- Paling umum (90% PC market share)
- User-friendly, support banyak software/games
- Cons: Bloatware, update sering annoying

**macOS**:
- Exclusive buat Apple hardware (MacBook, iMac)
- Clean UI, optimized (tight integration hardware + software)
- Cons: Mahal, limited software (ga semua apps/games available)

**Linux**:
- Open-source, free
- Powerful, customizable, favorite developer/server
- Cons: Learning curve steep (banyak via command line), support software consumer terbatas

**Coba perhatikan**:
- Waktu kamu buka app, OS yang load app dari storage ke RAM, terus instruksikan CPU buat jalanin.
- Waktu kamu save file, OS yang tulis data dari RAM ke storage.
- Waktu kamu copy file, OS yang manage operasi (read source → write destination).

---

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

**Coba perhatikan**:
- Semua ini happen **otomatis**. OS + Chrome handle complexity. Kamu cuma "ketik + enter".
- Ini kenapa **faster hardware = better experience**. CPU/RAM/SSD lebih cepat = workflow ini lebih cepat.

---

## Praktek

### Latihan 1: Inspect Komputer Kamu

**Tujuan**: Familiar dengan hardware komputer kamu (spec, usage).

**Yang Perlu Kamu Lakukan**:

**Windows**:
1. Buka **Task Manager** (Ctrl + Shift + Esc)
2. Tab **Performance**
3. Screenshot atau catat:
   - **CPU**: Model, speed, cores
   - **Memory (RAM)**: Total capacity, current usage
   - **Disk**: Type (SSD/HDD), capacity

**macOS**:
1. Buka **Activity Monitor** (Spotlight search → "Activity Monitor")
2. Tab **CPU**, **Memory**, **Disk**
3. Screenshot atau catat spec

**Atau via System Info**:
- **Windows**: Settings → System → About
- **Mac**: Apple menu →  About This Mac

**Expected Output**:

```
Komputer aku:
- CPU: Intel Core i5-8250U, 1.6 GHz, 4 cores
- RAM: 8 GB
- Storage: 256 GB SSD
```

**Acceptance Criteria**:
- [ ] Tau CPU model + cores
- [ ] Tau RAM capacity
- [ ] Tau storage type (SSD/HDD) + capacity

<details>
<summary>💡 Hints</summary>

**Hint 1**: Task Manager / Activity Monitor itu built-in tool di OS. Ga perlu install apa-apa.

**Hint 2**: Kalau CPU usage tinggi (>80%) padahal ga buka apa-apa, ada app/process yang consume banyak resource. Check tab **Processes** buat lihat mana yang makan banyak.

**Hint 3**: Kalau RAM usage hampir full, consider:
- Close apps yang ga dipake
- Restart komputer (clear memory leaks)
- Upgrade RAM (kalau sering multitasking berat)

</details>

<details>
<summary>✅ Solusi</summary>

Ga ada "solusi" fixed karena setiap komputer beda spec. Tapi **guideline**:

**CPU**:
- **Low-end**: Intel Celeron, Pentium, AMD A-series (browsing ringan aja)
- **Mid-range**: Intel i3, i5 / AMD Ryzen 3, 5 (coding, office, gaming ringan)
- **High-end**: Intel i7, i9 / AMD Ryzen 7, 9 (video editing, gaming berat, VM)

**RAM**:
- **4 GB**: Minimum (struggle kalau multitasking)
- **8 GB**: Sweet spot buat user biasa
- **16 GB+**: Comfortable buat developer/creator

**Storage**:
- **HDD**: Lambat tapi murah (good buat backup/archive)
- **SSD**: Cepat, upgrade paling worth it

**Action**: Kalau komputer kamu sering lag, prioritize upgrade:
1. **Upgrade SSD** (kalau masih HDD) - impact paling besar
2. **Add RAM** (kalau <8 GB dan sering multitask)
3. **CPU** (paling mahal, usually ga perlu upgrade kecuali CPU really old)

</details>

---

### Latihan 2: Monitoring Resource Usage Real-Time

**Tujuan**: Ngerti gimana apps consume resources (CPU, RAM, disk).

**Yang Perlu Kamu Lakukan**:

1. **Buka Task Manager / Activity Monitor** (tetap di tab Performance)

2. **Baseline** (komputer idle, no apps):
   - CPU usage: ~5-10%
   - RAM usage: ~2-3 GB (OS + background apps)

3. **Open apps satu-satu**, observe perubahan:
   - **Buka Chrome** (1 tab kosong):
     - RAM naik ~100-200 MB
     - CPU spike 10-20% (terus turun ke idle)
   - **Buka 10 tabs** (YouTube, Twitter, dll):
     - RAM naik ~500 MB - 1 GB
     - CPU usage naik (streaming video)
   - **Buka VS Code** (text editor):
     - RAM naik ~200-300 MB
     - CPU low (kecuali lagi compile code)
   - **Play video 4K di YouTube**:
     - CPU/GPU usage naik (decode video)

4. **Catat pattern**:
   - App mana yang paling "berat" (consume banyak RAM/CPU)?
   - Apa yang terjadi kalau RAM hampir full?

**Expected Output**:

```
Baseline (idle): CPU 5%, RAM 3 GB
Chrome (10 tabs): CPU 15%, RAM 4 GB (+1 GB)
Chrome + VS Code: CPU 20%, RAM 4.5 GB (+1.5 GB total)
Chrome + VS Code + YouTube 4K: CPU 40%, RAM 5 GB, GPU active
```

<details>
<summary>💡 Hints</summary>

**Hint 1**: Apps "heavy" itu relative. YouTube 4K berat buat laptop 4 GB RAM, tapi ringan buat desktop 16 GB RAM.

**Hint 2**: Kalau RAM full, OS pakai **disk swapping** (pakai storage sebagai RAM cadangan). Ini kenapa komputer jadi super lambat waktu RAM habis.

**Hint 3**: Chrome notorious sebagai "RAM eater". Tiap tab = process terpisah. 50 tabs = bisa 5+ GB RAM.

</details>

<details>
<summary>✅ Solusi + Insight</summary>

**Pattern yang kamu notice**:

1. **Apps modern consume banyak RAM** (Chrome, Slack, Electron apps). Ini kenapa 8 GB RAM sekarang "minimum comfortable".

2. **Video streaming/gaming consume CPU/GPU**. Decode video 4K butuh processing power.

3. **Background apps** (Windows Update, antivirus, Spotify) consume resource meskipun kamu ga aktif pake. Check tab **Processes** buat lihat.

**Real-world insight**:
- **Coding**: IDE (VS Code, PyCharm) + browser (documentation, Stack Overflow) + terminal = butuh 8 GB+ RAM comfortable.
- **Gaming**: CPU/GPU intensive. RAM 16 GB recommended.
- **Video editing**: RAM 16 GB+ (4K footage bisa 10+ GB RAM), CPU/GPU powerful.

**Action**:
- Kalau sering lag, **close apps yang ga dipake**. Jangan buka 50 tabs Chrome kalau cuma butuh 5.
- **Restart komputer** regular (clear memory leaks, refresh OS).
- **Disable startup apps** yang ga perlu (Windows: Task Manager → Startup; Mac: System Preferences → Users & Groups → Login Items).

</details>

---

### Latihan 3: File System Exploration

**Tujuan**: Ngerti structure file di komputer (folder, path, file types).

**Yang Perlu Kamu Lakukan**:

1. **Buka File Explorer** (Windows) atau **Finder** (Mac)

2. **Navigate ke folder penting**:

**Windows**:
- `C:\` (root drive, semua file ada di sini)
  - `C:\Users\[YourName]` (user folder)
    - `Documents` (dokumen kamu)
    - `Downloads` (file download)
    - `Desktop` (file di desktop)
  - `C:\Program Files` (aplikasi installed)
  - `C:\Windows` (OS files, jangan edit!)

**macOS**:
- `/` (root, ga perlu buka di Finder)
- `/Users/[YourName]` (user folder)
  - `Documents`, `Downloads`, `Desktop`
- `/Applications` (apps installed)
- `/System` (OS files, jangan edit!)

3. **Coba**:
   - Bikin folder baru di `Documents`: "test-folder"
   - Bikin file text: "hello.txt" (isi: "Hello World")
   - Copy file ke `Downloads`
   - Delete file di `Documents`
   - Check `Downloads` → file masih ada (copy, bukan move)

4. **Observe**:
   - File ada di storage (SSD/HDD)
   - Waktu kamu open file (double-click), OS load file dari storage → RAM → app (e.g., Notepad) buka

**Expected Output**:

```
Struktur folder aku:
C:\Users\Rapi\
  ├─ Documents\
  │   └─ test-folder\
  ├─ Downloads\
  │   └─ hello.txt (copied)
  └─ Desktop\
```

<details>
<summary>💡 Hints</summary>

**Hint 1**: **Path** itu alamat file. Contoh: `C:\Users\Rapi\Documents\hello.txt` (Windows) atau `/Users/Rapi/Documents/hello.txt` (Mac/Linux).

**Hint 2**: **Slash** beda:
- Windows: backslash `\`
- Mac/Linux: forward slash `/`

**Hint 3**: Ga perlu hafal semua folder. Yang penting tau:
- **User folder**: Tempat file personal kamu (Documents, Downloads, Desktop).
- **Program Files**: Aplikasi installed (ga perlu edit).
- **System folder** (Windows, System): OS files (NEVER edit unless you know what you're doing).

</details>

<details>
<summary>✅ Solusi + Insight</summary>

**Kenapa ini penting**:

1. **Waktu coding**, kamu bakal banyak kerja dengan files (save code, run script, import file). Ngerti file system = ga bingung "file aku di mana?".

2. **Path** itu konsep fundamental. Banyak error karena **wrong path** (file ga ketemu, app ga bisa load).

3. **Organize files** penting. Jangan taro semua di Desktop (slow, messy). Bikin folder structure yang make sense:
   ```
   Documents/
     ├─ Projects/
     │   ├─ project-1/
     │   └─ project-2/
     ├─ Learning/
     │   ├─ course-notes/
     │   └─ practice-code/
     └─ Personal/
   ```

**Real-world tip**:
- **Backup penting!** Storage bisa rusak (HDD fail, SSD corruption). Backup ke cloud (Google Drive, Dropbox) atau external drive.
- **Naming convention**: `project-name` (lowercase, dash) lebih baik dari `Project Name` (space bikin issue di command line nanti).

</details>

---

## Kesalahan Umum

### 1. Nganggep "Laptop Lambat" = Harus Beli Baru

**Contoh**:
> "Laptop aku lambat banget, ga bisa dipake. Kayaknya harus beli baru."

**Kenapa salah**:
Seringkali laptop "lambat" bukan karena hardware jelek, tapi:
- **RAM full** (terlalu banyak apps buka)
- **Storage full** (disk 90%+ full = slow)
- **Masih pakai HDD** (upgrade ke SSD = instant speed boost)
- **Malware/bloatware** (background apps makan resource)

**Cara bener**:
1. **Check resource usage** (Task Manager). Identify bottleneck (RAM, CPU, atau disk).
2. **Try upgrade dulu**:
   - Upgrade SSD (300-500rb buat 256 GB) = laptop kerasa 3x lebih cepat
   - Add RAM (kalau <8 GB)
3. **Clean up**:
   - Uninstall apps yang ga dipake
   - Scan malware (Windows Defender cukup)
   - Disable startup apps
4. **Reinstall OS** (last resort, tapi effective buat refresh).

Upgrade SSD + clean up often **lebih worth it** daripada beli laptop baru (save jutaan rupiah).

---

### 2. Ngira "Lebih Banyak Apps = Lebih Produktif"

**Contoh**:
> "Aku install 50 apps biar siap buat apapun. Tapi laptop kok jadi lambat ya?"

**Kenapa salah**:
Banyak apps = banyak yang jalan di background (consume RAM, CPU, disk). Most apps kamu install ga pernah dipake (bloat).

**Cara bener**:
- Install **cuma yang kamu actually pake** (minimal setup).
- Kalau jarang pake, **uninstall**. Kamu bisa reinstall kapan aja kalau butuh.
- Gunain **portable apps** atau **web apps** (ga perlu install, run from browser).

**Example minimalist setup** (coding):
- **Browser** (Chrome/Firefox)
- **Text editor** (VS Code)
- **Terminal** (built-in)
- **Git** (version control)

That's it. Install yang lain kalau actual butuh.

---

### 3. Save Semua File di Desktop

**Contoh**:
> "Desktop aku penuh 100+ file. Tapi gampang dicari, tinggal scroll."

**Kenapa salah**:
- **Slow**: OS render semua icon tiap boot/refresh. Desktop ratusan file = lag.
- **Messy**: Susah cari file (visual clutter).
- **Risky**: Kalau OS corrupt atau reinstall, Desktop sering ilang (kecuali di-backup).

**Cara bener**:
- **Desktop = temporary only**. File baru download/lagi dikerjain → taruh di Desktop sementara.
- **Setiap hari/minggu, move ke folder proper** (Documents/Projects/[category]).
- **Max 10-15 file di Desktop**. Lebih dari itu = time to organize.

**Folder structure recommended**:
```
Documents/
  ├─ Work/
  ├─ Personal/
  ├─ Learning/
  └─ Archive/
```

---

## Ringkasan

**Yang udah kamu pelajari**:

- **Komputer = Hardware + Software**. Hardware (fisik) + Software (instruksi) = sistem yang fungsional.
- **Hardware utama**:
  - **CPU**: Otak (process instruksi)
  - **RAM**: Meja kerja (data sementara, cepat)
  - **Storage**: Gudang (data permanen, lebih lambat)
  - **I/O devices**: Input (keyboard, mouse) + Output (monitor, speaker)
- **Software**:
  - **OS** (Windows, macOS, Linux): Koordinator semua hardware + apps
  - **Applications**: Tools spesifik (browser, editor, game)
  - **Drivers**: Penerjemah hardware
- **Workflow**: Input → CPU process (via RAM) → Output (di monitor)
- **Upgrade priority**: SSD > RAM > CPU (kalau laptop lambat)

**Key terms**:

- **Hardware**: Komponen fisik komputer (CPU, RAM, storage).
- **Software**: Instruksi/program yang jalanin hardware.
- **OS (Operating System)**: Software utama yang manage hardware + apps.
- **RAM**: Memory sementara (cepat, ilang waktu mati).
- **Storage**: Memory permanen (lambat, ga ilang).
- **CPU**: Processor yang eksekusi instruksi.
- **Path**: Alamat file di file system (e.g., `C:\Users\Rapi\Documents\file.txt`).

## Lanjut Kemana?

Sekarang kamu udah paham **apa yang ada di dalam komputer** dan **gimana cara kerjanya**. Next step: kita bakal belajar **cara "ngomong" ke komputer** via **command line** (terminal).

Command line itu interface text-based yang powerful banget buat developer. Lebih cepat dari klik-klik GUI, dan banyak tools development cuma available via command line.

**Lesson 3: "Command Line Basics - Ngobrol dengan Komputer via Text"** (coming soon)

Di lesson itu kita bakal belajar:
- Apa itu terminal/command line
- Navigation folder via terminal (cd, ls, pwd)
- File operations (mkdir, rm, cp, mv)
- Kenapa developer prefer terminal vs GUI

See you there! 🚀

---

**Punya pertanyaan?** Drop di [Discord Community](../../resources/community.md) atau open issue di [GitHub](https://github.com/muhammad-rapi/belajar-it-course/issues)
