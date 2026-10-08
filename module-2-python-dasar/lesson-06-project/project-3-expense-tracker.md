## Project 3: Expense Tracker

Track pemasukan & pengeluaran, calculate balance.

---

### Features

**MVP**:
1. Tambah transaksi (income/expense)
2. Lihat semua transaksi
3. Summary (total income, expense, balance)
4. Save to JSON

**Bonus**:
- Filter by category
- Date range filter
- Export to CSV
- Chart (matplotlib)

---

### Planning

**Data structure**:
```python
transactions = [
    {"id": 1, "type": "income", "amount": 5000000, "category": "Gaji", "date": "2024-01-15"},
    {"id": 2, "type": "expense", "amount": 500000, "category": "Makan", "date": "2024-01-16"}
]
```

**Functions**:
- `load_transactions()` → load from JSON
- `save_transactions(transactions)` → save
- `add_transaction(type, amount, category, date)` → tambah
- `view_transactions()` → print all
- `calculate_summary()` → total income/expense/balance

---

### Full Code

```python
import json
import os
from datetime import datetime

TRANSACTIONS_FILE = "transactions.json"

def load_transactions():
    if os.path.exists(TRANSACTIONS_FILE):
        with open(TRANSACTIONS_FILE, 'r') as f:
            return json.load(f)
    return []

def save_transactions(transactions):
    with open(TRANSACTIONS_FILE, 'w') as f:
        json.dump(transactions, f, indent=2)

def add_transaction(transactions, trans_type, amount, category, date=None):
    if date is None:
        date = datetime.now().strftime("%Y-%m-%d")
    
    trans_id = max([t["id"] for t in transactions], default=0) + 1
    transaction = {
        "id": trans_id,
        "type": trans_type,
        "amount": amount,
        "category": category,
        "date": date
    }
    transactions.append(transaction)
    save_transactions(transactions)
    print(f"✅ Transaksi ditambah: {trans_type} Rp {amount:,}")

def view_transactions(transactions):
    if not transactions:
        print("Belum ada transaksi")
        return
    
    for t in transactions:
        icon = "💰" if t["type"] == "income" else "💸"
        print(f"{icon} [{t['id']}] {t['date']} | {t['category']} | Rp {t['amount']:,}")

def calculate_summary(transactions):
    income = sum(t["amount"] for t in transactions if t["type"] == "income")
    expense = sum(t["amount"] for t in transactions if t["type"] == "expense")
    balance = income - expense
    
    print("\n=== Summary ===")
    print(f"💰 Total Income:  Rp {income:,}")
    print(f"💸 Total Expense: Rp {expense:,}")
    print(f"💵 Balance:       Rp {balance:,}")

def main():
    transactions = load_transactions()
    
    while True:
        print("\n=== Expense Tracker ===")
        print("1. Tambah transaksi")
        print("2. Lihat semua")
        print("3. Summary")
        print("4. Keluar")
        
        pilihan = input("Pilih (1-4): ")
        
        if pilihan == "1":
            trans_type = input("Type (income/expense): ").lower()
            if trans_type not in ["income", "expense"]:
                print("❌ Type harus 'income' atau 'expense'")
                continue
            
            amount = int(input("Amount (Rp): "))
            category = input("Category: ")
            add_transaction(transactions, trans_type, amount, category)
        
        elif pilihan == "2":
            view_transactions(transactions)
        
        elif pilihan == "3":
            calculate_summary(transactions)
        
        elif pilihan == "4":
            print("Bye!")
            break
        
        else:
            print("Pilihan ga valid")

if __name__ == "__main__":
    main()
```

---

### Testing

**Test flow**:
1. Tambah income (Gaji: 5,000,000)
2. Tambah expense (Makan: 500,000)
3. Tambah expense (Transport: 200,000)
4. View all
5. Summary → check balance (4,300,000)

---

### Bonus Challenges

**1. Filter by category**
```python
def filter_by_category(transactions, category):
    return [t for t in transactions if t["category"].lower() == category.lower()]
```

**2. Date range filter**
```python
from datetime import datetime

def filter_by_date_range(transactions, start_date, end_date):
    return [t for t in transactions 
            if start_date <= t["date"] <= end_date]
```

**3. Export to CSV**
```python
import csv

def export_to_csv(transactions, filename="transactions.csv"):
    with open(filename, 'w', newline='') as f:
        writer = csv.DictWriter(f, fieldnames=["id", "type", "amount", "category", "date"])
        writer.writeheader()
        writer.writerows(transactions)
    print(f"✅ Exported to {filename}")
```

**4. Chart** (perlu `pip install matplotlib`)
```python
import matplotlib.pyplot as plt

def plot_expenses_by_category(transactions):
    expenses = [t for t in transactions if t["type"] == "expense"]
    categories = {}
    for t in expenses:
        categories[t["category"]] = categories.get(t["category"], 0) + t["amount"]
    
    plt.pie(categories.values(), labels=categories.keys(), autopct='%1.1f%%')
    plt.title("Expenses by Category")
    plt.show()
```

---

Done! Lu punya expense tracker yang bisa track keuangan lu. 💰
