## Apa itu Terminal?

Terminal = **text-based interface** buat ngasih perintah ke komputer.

---

### Istilah yang Sering Bingung

**Terminal, Command Line, Shell, Console** - sebenernya beda, tapi orang sering pake interchangeably:

- **Terminal**: Aplikasi yang nge-run shell
- **Shell**: Program yang nerima command (bash, zsh, fish)
- **Command Line / CLI**: Interface text-based secara umum
- **Console**: Istilah lama, sekarang sama kayak terminal

**Praktis**: Sebut aja "terminal". Semua orang ngerti.

---

### Cara Buka Terminal

**macOS**:
- Spotlight (Cmd + Space) → ketik "Terminal"
- Atau: Applications → Utilities → Terminal

**Windows**:
- Win + R → ketik "cmd" → Enter (Command Prompt)
- Atau: Win + X → pilih "Windows Terminal" / "PowerShell"
- Lebih baik: Install [Git Bash](https://git-scm.com/downloads) (dapet bash shell kayak Mac/Linux)

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

**Parts**:
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

Selamat! Lu udah jalanin command pertama.

---

### Anatomy of a Command

```bash
ls -la /Users/rafi
```

**Parts**:
- `ls` = command (nama program)
- `-la` = flags/options (modify behavior)
- `/Users/rafi` = argument (input buat command)

---

### Command Shortcuts

**macOS/Linux/Git Bash**:
- `Tab` = autocomplete (ketik `cd Doc` terus Tab → jadi `cd Documents`)
- `↑` = command sebelumnya (history)
- `Ctrl + C` = stop command yang lagi jalan
- `Ctrl + L` = clear screen
- `Ctrl + D` = exit terminal

**Windows CMD**:
- Sama, tapi beberapa shortcut beda (misal: `Ctrl + L` ga jalan di CMD lama)

---

### Terminal itu Safe

Lu ga bakal rusak sistem cuma gara-gara typo. Contoh:

```bash
# Typo command
cdd Desktop  # Command not found (ga ada command 'cdd')
```

Terminal cuma bilang "ga ngerti command itu", ga bakal crash atau rusak apa-apa.

**Yang harus hati-hati**: Command yang **delete** atau **modify** file sistem. Tapi semua ada confirmation atau bisa di-undo.

---

Next: **Basic Commands** - ls, cd, pwd, mkdir.
