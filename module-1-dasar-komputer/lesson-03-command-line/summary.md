## Summary - Command Line Basics

Selamat! Lu udah bisa ngobrol sama komputer lewat terminal.

---

## Yang Udah Lu Pelajari

### Essential Commands

| Command | Fungsi | Contoh |
|---------|--------|--------|
| `pwd` | Liat posisi sekarang | `pwd` |
| `ls` | Liat isi folder | `ls -la` |
| `cd` | Pindah folder | `cd Documents` |
| `mkdir` | Bikin folder | `mkdir project` |
| `touch` | Bikin file | `touch app.py` |
| `rm` | Hapus | `rm file.txt` |
| `cp` | Copy | `cp a.txt b.txt` |
| `mv` | Move/rename | `mv old.txt new.txt` |
| `cat` | Liat isi file | `cat file.txt` |
| `clear` | Clear screen | `clear` |

### Path Types

- **Absolute**: Full path dari root (`/Users/rafi/Documents`)
- **Relative**: From current position (`../Documents`)
- **Symbols**: `.` (current), `..` (parent), `~` (home)

---

## Kenapa Ini Penting?

**Waktu lu belajar programming nanti**:

```bash
# Install library
npm install react

# Run Python script
python3 app.py

# Git workflow
git add .
git commit -m "Initial commit"
git push origin main

# Deploy ke server
ssh user@server
cd /var/www/app
git pull
npm run build
```

Semua itu **di terminal**. Ga ada GUI.

---

## Next Steps

**Next lesson: Internet & Web** - gimana data ngalir lewat internet.

Preview:
- Apa itu HTTP
- DNS (translate google.com → IP address)
- Client-server model
- Request-response cycle

Sebelum lanjut, **pastiin lu udah**:
- [ ] Comfortable buka terminal
- [ ] Hafal 10 command dasar
- [ ] Bisa navigasi pakai `cd`
- [ ] Paham absolute vs relative path

---

## Tips Biar Jago Terminal

**1. Sering-sering pake**

Daripada klik Finder/Explorer, pake terminal:
- Bikin folder? `mkdir`
- Buka file? `cd folder && code file.py`
- Cari file? `find . -name "*.py"`

**2. Customize prompt**

Install [Oh My Zsh](https://ohmyz.sh/) (macOS/Linux) atau [Oh My Posh](https://ohmyposh.dev/) (Windows) buat terminal lebih keren + helpful.

**3. Learn keyboard shortcuts**

- `Ctrl + A` = cursor ke awal line
- `Ctrl + E` = cursor ke akhir line
- `Ctrl + U` = hapus semua sebelum cursor
- `Ctrl + R` = search command history

**4. Alias untuk command sering dipake**

Tambahin di `~/.bashrc` atau `~/.zshrc`:

```bash
alias ll='ls -la'
alias gs='git status'
alias gp='git push'
```

Setelah itu, tinggal ketik `ll` instead of `ls -la`.

---

## Resources

**Belajar lebih dalam**:
- [Command Line Crash Course](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Understanding_client-side_tools/Command_line) - MDN
- [The Art of Command Line](https://github.com/jlevy/the-art-of-command-line) - GitHub guide

**Practice**:
- [cmdchallenge.com](https://cmdchallenge.com/) - Terminal challenges

---

Lu udah lewati mental block "takut terminal". Sekarang lu punya **superpowers** yang kebanyakan orang ga punya. 🚀

Next: Lesson 4 - Internet & Web!
