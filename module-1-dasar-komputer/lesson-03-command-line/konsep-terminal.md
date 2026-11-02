## Apa itu Terminal

Terminal adalah antarmuka berbasis teks buat ngasih perintah ke komputer.

---

### Istilah yang Sering Bingung

**Terminal, command line, shell, console**: sebenarnya beda, tapi orang sering memakainya bergantian.

- **Terminal**: aplikasi tempat lu ngetik
- **Shell**: program yang membaca dan menjalankan perintah lu (bash, zsh, PowerShell)
- **Command line** atau **CLI**: istilah umum buat antarmuka berbasis teks
- **Console**: istilah lama, sekarang artinya hampir sama dengan terminal

Sehari-hari cukup bilang "terminal". Semua orang ngerti.

---

### Cara Buka Terminal

**macOS**:
- Spotlight (Cmd + Space) → ketik "Terminal"
- Atau: Applications → Utilities → Terminal

**Windows**:
- Win + R → ketik "cmd" → Enter (Command Prompt)
- Atau: Win + X → pilih "Windows Terminal" / "PowerShell"
- Alternatif yang disarankan buat belajar: pasang [Git Bash](https://git-scm.com/downloads), supaya perintahnya sama dengan macOS dan Linux. Cara pasangnya dibahas di Lesson 6.

**Linux**:
- Ctrl + Alt + T
- Atau cari "Terminal" di app menu

---

### Tampilan Terminal

Begitu lu buka terminal, lu liat yang kayak gini:

**macOS/Linux**:
```
mac@Macbook ~ %
```

**Windows (PowerShell)**:
```
PS C:\Users\Rafi>
```

**Git Bash (Windows)**:
```
Rafi@DESKTOP-ABC ~/
$
```

**Bagian-bagiannya**:
- `mac` / `Rafi` = username
- `Macbook` / `DESKTOP-ABC` = hostname (nama komputer)
- `~` / `C:\Users\Rafi` = current directory
- `%` / `>` / `$` = prompt (tanda siap terima command)

---

### Ngetes Terminal

Coba ketik:

```bash
echo "Hello World"
```

Terus Enter. Output:

```
Hello World
```

Itu command pertama lu.

---

### Bagian-Bagian Sebuah Perintah

```bash
ls -la /Users/rafi
```

**Parts**:
- `ls`: nama perintah
- `-la`: opsi (flag) yang mengubah cara kerja perintah
- `/Users/rafi`: argumen, yaitu bahan yang dikerjakan perintah

---

### Pintasan Keyboard

**macOS/Linux/Git Bash**:
- `Tab` = melengkapi nama otomatis (ketik `cd Doc` lalu Tab, jadi `cd Documents`)
- `↑` = perintah sebelumnya
- `Ctrl + C` = stop command yang lagi jalan
- `Ctrl + L` = clear screen
- `Ctrl + D` = keluar dari terminal

**Windows CMD**:
- Sama, tapi beberapa shortcut beda (misal: `Ctrl + L` nggak jalan di CMD lama)

---

### Seberapa Aman Terminal

Lu nggak bakal rusak sistem cuma gara-gara typo. Contoh:

```bash
# Typo command
cdd Desktop  # Command not found (nggak ada command 'cdd')
```

Terminal cuma bilang "nggak ngerti command itu", nggak bakal crash atau rusak apa-apa.

**Yang harus hati-hati**: command yang menghapus atau mengubah file, seperti `rm`. Command itu jalan tanpa konfirmasi dan nggak ada Recycle Bin. File yang kehapus lewat terminal nggak bisa dibalikin dengan gampang.

---

Berikutnya: perintah dasar seperti `ls`, `cd`, `pwd`, dan `mkdir`.
