
# 🚆 Railway Reservation System

A comprehensive **Railway Reservation System** developed in **C++ (Console)** and **Python (Tkinter GUI)** that enables users and admins to manage train ticket bookings, station listings, and reservations. Ideal for academic projects or as a prototype for larger transportation systems.

---

## 📁 Project Structure

```
.
├── header.h               # Class & structure definitions
├── management.cpp         # Core logic (reservations, users, date handling)
├── main.cpp               # Application flow for admin & user roles (C++ CLI)
├── railway_gui.py         # Python Tkinter GUI for ticketing
├── bookings.csv           # (Generated) Stores user bookings from GUI
├── stations.txt           # List of available stations (for GUI)
└── user.dat / adm.bin     # Binary storage for users and system data (CLI)
```

---

## 🚀 Features

### C++ Console Application
- **Admin Features:**
  - Add/delete/view railway stations
  - View all reservations
  - Set or update base fare
- **User Features:**
  - Book a train ticket
  - Cancel an existing reservation
  - Generate a ticket number automatically
- **Data Persistence:** Uses `fstream` to store user credentials, stations, and bookings in binary/text files

### Python GUI Application
- **Modern Interface:** Built with `Tkinter` and `tkcalendar`
- **User-friendly booking flow**
- **Admin Panel:**
  - Manage stations
  - View bookings
- **CSV-based Data Storage** for simplicity and portability

---

## 🔧 Requirements

### For C++ Version:
- Windows OS (due to `<conio.h>` and `<Windows.h>`)
- C++11 or later
- A C++ compiler (e.g., GCC, MSVC)

### For Python GUI Version:
- Python 3.6+
- Install dependencies:
  ```bash
  pip install tk tkcalendar
  ```

---

## 🎮 How to Run

### ✅ C++ Console Version

1. Compile:
   ```bash
   g++ main.cpp management.cpp -o railway.exe
   ```

2. Run:
   ```bash
   ./railway.exe
   ```

3. On first run:
   - You’ll be prompted to set up admin and user accounts
   - The system stores them in `user.dat`

---

### ✅ Python GUI Version

1. Run the GUI:
   ```bash
   python railway_gui.py
   ```

2. Use:
   - Login as `admin / admin123` for station management
   - Login as `user / user123` for booking tickets

---

## 🔐 Authentication

| Role   | Username | Password  |
|--------|----------|-----------|
| Admin  | admin    | admin123  |
| User   | user     | user123   |

> **Note:** C++ credentials are stored in a binary file, while Python GUI uses hardcoded values (you can enhance this as needed).

---

## 🧠 Ticket Generation Logic (C++)

Ticket number = First character of source + destination + date in `DDMMYY` + class type  
Example: `DLKT050825E` (from Delhi to Kolkata on 5th Aug 2025 in Economy)

---

## 📌 Future Enhancements

- Add route and time management
- Integrate payment methods
- Migrate data storage to SQLite or MySQL
- Multi-language support
- Use encryption for passwords

---

## 📷 Screenshots

> Add screenshots here of the GUI and console interface for better visual understanding.

---

## 📜 License

This project is for educational purposes and is licensed under the MIT License.

---

## 👨‍💻 Authors

- **C++ System Developer**: *Your Name Here*
- **Python GUI Developer**: *Your Name Here*

> Replace names with actual contributors if collaborating.
