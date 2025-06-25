# 📝 Oddiy To-Do List App (CLI + JSON)

## 🎯 Loyiha haqida

Ushbu loyiha oddiy terminal interfeysida ishlaydigan to-do list (vazifalar ro‘yxati) dasturidir. Dastur foydalanuvchidan vazifalarni qabul qiladi, ularni faylga saqlaydi, ko‘rsatadi, o‘chiradi va bajarilgan deb belgilaydi. Ma’lumotlar `.json` faylida saqlanadi.

Loyiha kichik bo‘lsa ham, quyidagi muhim konseptlarni o‘rgatadi:

* Modul bilan ishlash
* CLI interfeys yaratish
* Fayl bilan ishlash
* JSON formati
* Funksional struktura
* Rangli terminal (`termcolor`)

---

## 🛠 Texnologiyalar

| Texnologiya | Izoh                                     |
| ----------- | ---------------------------------------- |
| Python 3    | Asosiy dasturlash tili                   |
| JSON        | Ma’lumotlarni saqlash formati            |
| termcolor   | Rangli terminal chiqishi uchun kutubxona |

---

## 📁 Loyiha tuzilmasi (strukturasi)

```
Python-Simple-ToDo-List/
├── app/
│   ├── __init__.py          # Modul sifatida ko‘rish uchun
│   ├── main.py              # CLI menyu interfeysi
│   ├── core.py              # Biznes mantiq (CRUD)
│   └── utils.py             # Fayl (JSON) bilan ishlash
│
├── data/
│   └── tasks.json           # Barcha vazifalar shu faylda saqlanadi
│
├── run.py                   # Loyihani ishga tushirish uchun fayl
├── README.md                # Loyiha tavsifi (shu fayl)
└── requirements.txt         # Kutubxonalar ro‘yxati
```

---

## ✅ BOSHQICHMA-BOSHQICH TOPSHIRIQLAR

### 📌 1-Topshiriq: Loyiha strukturasi yaratish

* `Python-Simple-ToDo-List/` nomli papka oching
* Unda `app/`, `data/` papkalarini yarating
* `run.py`, `README.md`, `requirements.txt` fayllarini yarating

---

### 📌 2-Topshiriq: JSON fayl orqali ma’lumot saqlash

* `data/tasks.json` faylini yarating
* Unga bo‘sh ro‘yxat yozing: `[]`
* Keyinchalik barcha vazifalar shu faylda saqlanadi

---

### 📌 3-Topshiriq: `termcolor` kutubxonasini o‘rnatish

```bash
pip install termcolor
```

* `requirements.txt` faylga quyidagini yozing:

```
termcolor
```

---

### 📌 4-Topshiriq: `utils.py` faylida fayl bilan ishlovchi funksiyalar yozing

* `load_data()` – `data/tasks.json` faylidan ro‘yxatni o‘qib qaytarsin
* `save_data(tasks)` – ro‘yxatni faylga saqlab qo‘ysin

---

### 📌 5-Topshiriq: `core.py` faylida asosiy funksiyalarni yozing

* `add_task()` – yangi vazifa qo‘shish
* `list_tasks()` – barcha vazifalarni chiqarish
* `complete_task()` – vazifani bajarilgan deb belgilash
* `delete_task()` – vazifani o‘chirish

---

### 📌 6-Topshiriq: `main.py` faylida menyu yozing

* CLI menyu bo‘lishi kerak:

```
1. Vazifalarni ko‘rish
2. Vazifa qo‘shish
3. Vazifani bajarildi deb belgilash
4. Vazifani o‘chirish
5. Chiqish
```

* Foydalanuvchi tanlov kiritganda, `core.py`dagi tegishli funksiyani chaqiring

---

### 📌 7-Topshiriq: `run.py` orqali ishga tushirish

* `run.py` faylida `from app.main import run_cli` deb menyuni ishga tushiring

```python
# run.py
from app.main import run_cli

if __name__ == "__main__":
    run_cli()
```

---

### 📌 8-Topshiriq: Rangli terminal chiqishi (termcolor)

* `termcolor` yordamida:

  * `bajarilgan` vazifalarni yashil
  * `bajarilmagan` vazifalarni sariq
  * `xatoliklar`ni qizil rangda chiqaring

---

## 💡 BONUS TOPSHIRIQLAR

* [ ] Har bir vazifaga **yaratilgan sana** qo‘shish
* [ ] `id` lar avtomatik oshib boradigan tarzda ishlasin
* [ ] `deadline` qo‘shish (sana formatida)
* [ ] `bajarilganlar soni` va `umumiy vazifalar soni`ni ko‘rsatish
* [ ] `qidiruv` funksiyasi yozish (`title` bo‘yicha)

---

## 🚀 Dasturdan foydalanish

```bash
python run.py
```

---
 hohlasangiz, har bir `.py` faylni ham `task-based` yozib beraman. Ayting?
