
# 🤖 TeleBotOrder

A Telegram-based order management system for managing users, buy/sell orders, permissions, transactions, and daily reports.

The project was developed around a real-world trading workflow with user approval, permission management, order validation, transaction tracking, and automated reporting.

## 🚀 Features

- 👤 User registration and admin approval
- 🔐 Role-based permission management
- 📊 Buy and sell order management
- ⏱️ Order expiration and cancellation
- 📦 Daily trading capacity limits
- 📅 Persian calendar, holidays, and working hours
- 🤝 Order acceptance and transaction tracking
- 📄 Automated PDF transaction reports
- 👨‍💼 Admin panel for user and system management

## 🧰 Tech Stack

- **Python**
- **aiogram 3**
- **SQLite**
- **Jinja2**
- **WeasyPrint**
- **PersianTools**
- **python-dotenv**
- **Git**

## 🏗️ Project Structure

```text
TeleBotOrder/
├── handlers/       # User, admin and order handlers
├── keyboards/      # Telegram keyboards
├── states/         # FSM states
├── utils/          # Parser, reports and date utilities
├── fonts/          # Persian font
├── database.py     # Database operations
├── config.py       # Configuration
├── main.py         # Application entry point
└── requirements.txt
````

## 🔄 Order Workflow

```text
User
  ↓
Submit Order
  ↓
Validation
  ↓
Confirmation
  ↓
Publish to Channel
  ↓
Order Acceptance
  ↓
Transaction Record
  ↓
PDF Report
```

## ⚙️ Installation

```bash
git clone https://github.com/Farzaneh-Nasrabadii/TeleBotOrder.git
cd TeleBotOrder

python3 -m venv .venv
source .venv/bin/activate

pip install -r requirements.txt
cp .env.example .env
```

Configure the required environment variables and run:

```bash
python3 main.py
```

## 🔐 Security

Sensitive configuration is stored in environment variables and excluded from version control.

Local databases and generated reports are also excluded from Git.

## 📌 Project Status

Production-oriented Telegram order management system currently under active development.

## 👩‍💻 Author

**Farzaneh Nasrabadi**

Backend Developer | Python | Java | PostgreSQL | Linux

[GitHub](https://github.com/Farzaneh-Nasrabadii) ·
[LinkedIn](https://www.linkedin.com/in/farzaneh-nasrabadii/)
