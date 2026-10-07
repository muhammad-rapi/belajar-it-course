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