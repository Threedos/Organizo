# 🚀 Organizo — Agile Project Management API

Organizo is a **Laravel-based REST API** for an Agile project management system that supports projects, sprints, tasks, collaboration, subscriptions, and payments.

It is designed as a **backend-only SaaS system** (no frontend included).

---

# 📌 Features

* Authentication (JWT / Sanctum)
* Email verification (OTP)
* Forgot password (OTP)
* Project management
* Sprint management
* Task tracking system
* Team collaboration
* Comments & attachments
* Personal notes
* Subscription plans
* Payment integration (Paymob-ready)
* Role-based access control

---

# 🧱 Tech Stack

* Laravel 11+
* MySQL
* Sanctum / JWT
* SMTP (Mailtrap / Gmail)
* Paymob (for payments)

---

# ⚙️ Installation Guide

## 1. Clone the project

```bash
git clone https://github.com/your-username/organizo.git
cd organizo
```

---

## 2. Install dependencies

```bash
composer install
```

---

## 3. Copy environment file

```bash
cp .env.example .env
```

---

## 4. Generate application key

```bash
php artisan key:generate
```

---

## 5. Configure database

Edit `.env`:

```env
DB_DATABASE=organizo
DB_USERNAME=root
DB_PASSWORD=
```

Then run:

```bash
php artisan migrate
```

---

## 6. Run the server

```bash
php artisan serve
```

API will be available at:

```
http://127.0.0.1:8000
```

---

# 📧 Email Setup (OTP System)

Organizo uses SMTP for OTP verification and password reset.

Example (Mailtrap):

```env
MAIL_MAILER=smtp
MAIL_HOST=sandbox.smtp.mailtrap.io
MAIL_PORT=2525
MAIL_USERNAME=your_username
MAIL_PASSWORD=your_password
MAIL_ENCRYPTION=tls
MAIL_FROM_ADDRESS=noreply@organizo.com
MAIL_FROM_NAME="Organizo"
```

---

# 🔐 Authentication Flow

### Register

```
POST /api/register
```

### Verify Email (OTP)

```
POST /api/verify-email
```

### Login

```
POST /api/login
```

### Forgot Password

```
POST /api/forgot-password
```

### Reset Password

```
POST /api/reset-password
```

---

# 📦 Core Modules

## 🏗 Projects

* Create project
* Update project
* Delete project
* Add members

## 🧩 Sprints

* Create sprint
* Manage sprint timeline

## ✅ Tasks

* Assign tasks
* Change status (Todo → Done)
* Archive tasks

## 💬 Collaboration

* Comments
* Attachments

## 📝 Notes

* Private user notes

---

# 💳 Subscription System

Organizo supports SaaS plans:

* Free
* Basic
* Pro

Each plan controls:

* Max projects
* Max team members
* Feature access

---

# 💰 Payment Integration

Organizo is ready for:

Paymob

Used for:

* Subscription payments
* Plan upgrades

---

# 📡 API Response Format

All responses follow this structure:

```json
{
  "success": true,
  "message": "Operation successful",
  "data": {}
}
```

---

# 🧪 Testing API

Use Postman or any API client.

Base URL:

```
http://127.0.0.1:8000/api
```

---

# 📁 Project Structure (Recommended)

```
app/
 ├── Http/
 ├── Models/
 ├── Services/
 ├── Repositories/
 ├── Mail/
 ├── Actions/
```

---

# 🚧 Development Phases

* Phase 1: Database design
* Phase 2: Authentication system
* Phase 3: Projects & Teams
* Phase 4: Sprints & Tasks
* Phase 5: Collaboration
* Phase 6: Subscription & Payments

---

# ⚠️ Notes

* This project is backend-only (API)
* No frontend included
* Designed for learning + SaaS architecture practice
* Built for scalability and clean architecture

---

# 📜 License

This project is for educational purposes.

---

# 👨‍💻 Author

Organizo Team
:::
Team 2 Season'24
