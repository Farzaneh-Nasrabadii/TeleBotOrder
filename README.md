
# TeleBotOrder

A Telegram-based order management system built with **Python** and **Aiogram 3**.

The system allows users to create and accept orders through Telegram while providing administrators with user management, permission control, capacity management, order monitoring, and transaction reporting.

## Features

- User registration and approval workflow
- Admin user management
- Permission-based access control
- Order creation and confirmation
- Order acceptance and partial fulfillment
- Order expiration and cancellation
- Daily user capacity limits
- Configurable working hours
- Holiday management
- Telegram channel integration
- Admin transaction notifications
- PDF transaction reports
- Persian date and time support
- SQLite database
- Asynchronous Telegram bot architecture

## Tech Stack

- **Python 3**
- **Aiogram 3**
- **SQLite**
- **Jinja2**
- **WeasyPrint**
- **python-dotenv**
- **Persian date/time handling**
- **HTML / CSS**
- **Git**

## Project Structure

```text
TeleBotOrder/
│
├── handlers/
│   ├── admin.py
│   ├── callbacks.py
│   ├── order.py
│   └── user.py
│
├── keyboards/
│   ├── inline.py
│   └── reply.py
│
├── states/
│   └── order.py
│
├── utils/
│   ├── parser.py
│   ├── report_generator.py
│   ├── admin_report_generator.py
│   └── today_iran_timestamps.py
│
├── fonts/
│   └── Vazirmatn.ttf
│
├── config.py
├── database.py
├── main.py
├── requirements.txt
└── README.md
````

## How It Works

### 1. User Registration

New users can register through Telegram and wait for administrator approval.

### 2. Permissions

Administrators can control user permissions, including:

* Creating orders
* Accepting orders

User status and permissions are checked before performing protected operations.

### 3. Creating an Order

Authorized users can submit an order through Telegram.

The system validates:

* Order format
* User status
* User permissions
* Daily capacity
* Working hours
* Holidays
* Price limits
* Existing active orders

After validation, the order is shown to the user for confirmation.

### 4. Order Acceptance

Other authorized users can accept available orders.

The system tracks:

* Accepted quantity
* Remaining quantity
* Acceptor
* Order owner
* Transaction time
* Transaction identifier

When the remaining quantity reaches zero, the order is completed.

### 5. Administration

Administrators can manage:

* Users
* User status
* Permissions
* Daily capacity
* Working hours
* Holidays
* Transaction reports

### 6. Reporting

The system generates PDF reports containing transaction information for administrative use.

## Configuration

Create a `.env` file in the project root:

```env
BOT_TOKEN=your_bot_token
CHANNEL_ID=your_channel_id
ADMIN_CHANNEL_ID=your_admin_channel_id
ADMIN_ID=your_admin_ids
```

Never commit `.env` or other secrets to the repository.

## Installation

Clone the repository:

```bash
git clone https://github.com/Farzaneh-Nasrabadii/TeleBotOrder.git
cd TeleBotOrder
```

Create a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Configure the environment variables:

```bash
cp .env.example .env
```

Edit `.env` and add your Telegram bot configuration.

## Running the Bot

```bash
python3 main.py
```

## Security

Sensitive configuration and local database files are excluded from version control.

The project uses environment variables for credentials and configuration values.

## License

This project is licensed under the MIT License.

## Author

**Farzaneh Nasrabadi**

Backend Developer | Python | Java | PostgreSQL | Docker

GitHub:
[https://github.com/Farzaneh-Nasrabadii](https://github.com/Farzaneh-Nasrabadii)
