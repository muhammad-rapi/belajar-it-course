# File Permissions

## Apa itu Permissions?

**Permissions** = aturan siapa boleh **baca**, **edit**, atau **hapus** file/folder.

**Analogi**: Kamar kos kamu punya aturan:
- **Kamu (owner)**: boleh masuk, tidur, ubah furniture (full access)
- **Teman (group)**: boleh masuk, duduk, tapi ga boleh pindahin kasur (read + limited write)
- **Stranger (others)**: ga boleh masuk sama sekali (no access)

File di komputer works sama.

---

## Permissions di Windows

Windows lebih sederhana: file punya **attributes**.

**Attributes**:
- **Read-only**: File cuma bisa dibaca, ga bisa diedit atau dihapus
- **Hidden**: File disembunyiin dari File Explorer
- **System**: File penting buat OS

**Cara lihat/ubah**:
1. Klik kanan file → **Properties**
2. Tab **General** → lihat di bagian **Attributes**

---

## Permissions di macOS/Linux

macOS & Linux punya sistem permissions lebih detail.

### 3 Permissions:
- **Read** (r): Bisa baca isi file
- **Write** (w): Bisa edit atau hapus file
- **Execute** (x): Bisa run file (kalo file adalah program/script)

### 3 User Categories:
- **Owner** (u): user yang bikin file
- **Group** (g): grup yang assigned ke file
- **Others** (o): semua user lain

**Notasi**: `rwxr-xr--`

Breakdown:
```
rwx  r-x  r--
│││  │││  │││
│││  │││  └└└─ Others: read only
│││  └└└─────── Group: read + execute
└└└──────────── Owner: read + write + execute
```

**Cara lihat**:
```bash
ls -l file.txt
-rw-r--r--  1 rafi  staff  1234 Oct 7 file.txt
```

**Cara ubah**:
```bash
chmod 755 script.sh    # Owner: rwx, Group: r-x, Others: r-x
chmod +x script.sh     # Tambah execute permission
chmod 600 config.json  # Cuma owner yang bisa read/write
```

---

## Best Practices

### 1. Principle of Least Privilege
Jangan kasih more permission than needed.

❌ Bad: `chmod 777` (everyone can read/write/execute)  
✅ Good: `chmod 644` untuk document (owner write, others read)

### 2. Protect Sensitive Files
```bash
chmod 600 ~/.ssh/id_rsa    # Private SSH key (owner-only)
```

### 3. Executable Scripts
```bash
chmod 755 deploy.sh   # Owner can edit+run, others can only run
```

---

## Kesalahan Umum

### chmod 777 Everything
**Masalah**: Semua orang (even malware) bisa edit file kamu.

**Fix**: Pakai permission yang reasonable (644 for files, 755 for folders).

### Forget to Make Script Executable
**Masalah**: Download script, run, error "Permission denied".

**Fix**: `chmod +x script.sh` dulu.

---

Lanjut ke [Exercises →](./exercises.md)
