## Project 1: File Organizer

Organize files di folder berdasarkan extension.

---

### Problem

Download folder lu berantakan: 100+ files campur aduk (.jpg, .pdf, .txt, .mp4, dll).

**Manual**:
- Bikin folder "Images", "Documents", "Videos"
- Drag-drop satu-satu

**Automation**: Script Python yang organize otomatis.

---

### Features

**MVP (Minimum Viable Product)**:
1. Scan folder
2. Group by extension
3. Move files ke folder sesuai tipe

**Bonus**:
- Duplicate detection
- Dry run (preview sebelum move)
- Undo feature

---

### Planning

**Data structure**:
```python
file_types = {
    "Images": [".jpg", ".jpeg", ".png", ".gif"],
    "Documents": [".pdf", ".doc", ".docx", ".txt"],
    "Videos": [".mp4", ".avi", ".mkv"],
    "Audio": [".mp3", ".wav", ".flac"]
}
```

**Functions**:
- `get_files(folder)` → list files
- `get_extension(filename)` → extension
- `get_folder_for_file(extension)` → target folder
- `move_file(src, dst)` → move file
- `organize(folder)` → main logic

---

### Starter Code

```python
import os
import shutil

FILE_TYPES = {
    "Images": [".jpg", ".jpeg", ".png", ".gif", ".bmp"],
    "Documents": [".pdf", ".doc", ".docx", ".txt", ".xlsx"],
    "Videos": [".mp4", ".avi", ".mkv", ".mov"],
    "Audio": [".mp3", ".wav", ".flac", ".aac"],
    "Archives": [".zip", ".rar", ".tar", ".gz"]
}

def get_extension(filename):
    """Get file extension (lowercase)"""
    return os.path.splitext(filename)[1].lower()

def get_folder_for_file(extension):
    """Return folder name for extension"""
    for folder, extensions in FILE_TYPES.items():
        if extension in extensions:
            return folder
    return "Others"

def organize_files(source_folder):
    """Organize files in source_folder"""
    files = os.listdir(source_folder)
    
    for filename in files:
        file_path = os.path.join(source_folder, filename)
        
        # Skip directories
        if os.path.isdir(file_path):
            continue
        
        # Get extension & target folder
        ext = get_extension(filename)
        folder = get_folder_for_file(ext)
        
        # Create target folder if not exist
        target_folder = os.path.join(source_folder, folder)
        os.makedirs(target_folder, exist_ok=True)
        
        # Move file
        target_path = os.path.join(target_folder, filename)
        shutil.move(file_path, target_path)
        print(f"Moved: {filename} → {folder}/")

# Run
if __name__ == "__main__":
    folder = input("Masukkan path folder: ")
    if os.path.exists(folder):
        organize_files(folder)
        print("✅ Done!")
    else:
        print("❌ Folder ga ada")
```

---

### Testing

**Test folder**:
```bash
mkdir test_folder
cd test_folder
touch photo1.jpg document.pdf video.mp4 song.mp3 file.txt
```

**Run**:
```bash
python file_organizer.py
# Input: test_folder
```

**Result**:
```
test_folder/
├── Images/
│   └── photo1.jpg
├── Documents/
│   ├── document.pdf
│   └── file.txt
├── Videos/
│   └── video.mp4
└── Audio/
    └── song.mp3
```

---

### Bonus Challenges

**1. Dry run mode**
```python
def organize_files(source_folder, dry_run=False):
    # Preview changes tanpa move
    if dry_run:
        print(f"[DRY RUN] Would move: {filename} → {folder}/")
    else:
        shutil.move(file_path, target_path)
```

**2. Duplicate detection**
```python
import hashlib

def get_file_hash(filepath):
    with open(filepath, 'rb') as f:
        return hashlib.md5(f.read()).hexdigest()

# Compare hashes before move
```

**3. Undo feature**
Save move history ke JSON, implement `undo()`.

---

Done! Lu punya automation script yang save waktu berjam-jam. 🎉
