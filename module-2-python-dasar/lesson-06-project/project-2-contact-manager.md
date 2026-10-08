## Project 2: Contact Manager CLI

CRUD (Create, Read, Update, Delete) contacts dengan save ke JSON.

---

### Features

**MVP**:
1. Tambah contact (nama, no HP, email)
2. Lihat semua contacts
3. Cari contact by nama
4. Hapus contact
5. Save/load dari JSON

**Bonus**:
- Edit contact
- Export to CSV
- Import from CSV

---

### Planning

**Data structure**:
```python
contacts = [
    {"id": 1, "name": "Rafi", "phone": "08123456789", "email": "rafi@mail.com"},
    {"id": 2, "name": "Budi", "phone": "08198765432", "email": "budi@mail.com"}
]
```

**Functions**:
- `load_contacts()` → load dari JSON
- `save_contacts(contacts)` → save ke JSON
- `add_contact(name, phone, email)` → tambah
- `view_contacts()` → print all
- `search_contact(name)` → cari
- `delete_contact(id)` → hapus

---

### Starter Code

```python
import json
import os

CONTACTS_FILE = "contacts.json"

def load_contacts():
    """Load contacts from JSON file"""
    if os.path.exists(CONTACTS_FILE):
        with open(CONTACTS_FILE, 'r') as f:
            return json.load(f)
    return []

def save_contacts(contacts):
    """Save contacts to JSON file"""
    with open(CONTACTS_FILE, 'w') as f:
        json.dump(contacts, f, indent=2)

def add_contact(contacts, name, phone, email):
    """Add new contact"""
    contact_id = max([c["id"] for c in contacts], default=0) + 1
    contact = {
        "id": contact_id,
        "name": name,
        "phone": phone,
        "email": email
    }
    contacts.append(contact)
    save_contacts(contacts)
    print(f"✅ Contact '{name}' ditambah")

def view_contacts(contacts):
    """Display all contacts"""
    if not contacts:
        print("Ga ada contact")
        return
    
    for c in contacts:
        print(f"[{c['id']}] {c['name']} | {c['phone']} | {c['email']}")

def search_contact(contacts, name):
    """Search contact by name"""
    results = [c for c in contacts if name.lower() in c["name"].lower()]
    if results:
        for c in results:
            print(f"[{c['id']}] {c['name']} | {c['phone']} | {c['email']}")
    else:
        print("Ga ketemu")

def delete_contact(contacts, contact_id):
    """Delete contact by ID"""
    for i, c in enumerate(contacts):
        if c["id"] == contact_id:
            deleted = contacts.pop(i)
            save_contacts(contacts)
            print(f"✅ Contact '{deleted['name']}' dihapus")
            return
    print("❌ ID ga ketemu")

def main():
    contacts = load_contacts()
    
    while True:
        print("\n=== Contact Manager ===")
        print("1. Tambah contact")
        print("2. Lihat semua")
        print("3. Cari contact")
        print("4. Hapus contact")
        print("5. Keluar")
        
        pilihan = input("Pilih (1-5): ")
        
        if pilihan == "1":
            name = input("Nama: ")
            phone = input("No HP: ")
            email = input("Email: ")
            add_contact(contacts, name, phone, email)
        
        elif pilihan == "2":
            view_contacts(contacts)
        
        elif pilihan == "3":
            name = input("Cari nama: ")
            search_contact(contacts, name)
        
        elif pilihan == "4":
            contact_id = int(input("ID contact: "))
            delete_contact(contacts, contact_id)
        
        elif pilihan == "5":
            print("Bye!")
            break
        
        else:
            print("Pilihan ga valid")

if __name__ == "__main__":
    main()
```

---

### Testing

**Run**:
```bash
python contact_manager.py
```

**Test flow**:
1. Tambah 3 contacts
2. Lihat semua → cek JSON file
3. Cari by nama
4. Hapus 1 contact
5. Check `contacts.json` file

---

### Bonus Challenges

**1. Edit contact**
```python
def edit_contact(contacts, contact_id, name=None, phone=None, email=None):
    for c in contacts:
        if c["id"] == contact_id:
            if name: c["name"] = name
            if phone: c["phone"] = phone
            if email: c["email"] = email
            save_contacts(contacts)
            print("✅ Contact diupdate")
            return
```

**2. Export to CSV**
```python
import csv

def export_to_csv(contacts, filename="contacts.csv"):
    with open(filename, 'w', newline='') as f:
        writer = csv.DictWriter(f, fieldnames=["id", "name", "phone", "email"])
        writer.writeheader()
        writer.writerows(contacts)
    print(f"✅ Exported to {filename}")
```

**3. Validation**
- Email format check (regex)
- Phone number format (08xxx)
- Duplicate detection

---

Done! Lu punya contact manager yang fully functional. 📇
