# 🐘 + 🗃️ Task 3: PHP Advanced Form Validation, Authentication & Admin Panel

## Modules Covered

* Module 1: Introduction to PHP & MySQL Integration
* Module 5: Connecting PHP with MySQL
* Module 6: CRUD Operations with PHP & MySQL
* Module 8: Authentication and Login System
* Module 9: Creating a Database Class in PHP
* Module 14: Advanced CRUD Features (MySQLi + OOP)

---
<img width="1123" height="631" alt="image" src="https://github.com/user-attachments/assets/afa23460-d492-4a3e-8ec1-85c5b194dcc3" />


## 🎯 Goal

Build a **PHP + MySQL** web application with:

* **Landing page**
* **User registration** with advanced validation (frontend + backend)
* **User login** with roles (Admin/User)
* **Welcome page**
* **Admin panel** with full CRUD for users

---

## Steps

### **1. Create the Database**

```sql
CREATE DATABASE php_advanced_auth;

USE php_advanced_auth;

CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    full_name VARCHAR(255) NOT NULL,
    email VARCHAR(100) NOT NULL UNIQUE,
    phone VARCHAR(20) NOT NULL,
    password VARCHAR(255) NOT NULL,
    role ENUM('Admin','User') DEFAULT 'User',
    date_created TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    user_image VARCHAR(255) DEFAULT NULL
);
```

* Create one **Admin user** manually with hashed password.

---

### **2. Landing Page**

* File: `index.php`
* Display:

  * Welcome message
  * Links to `login.php` and `signup.php`

---

### **3. Sign-Up Page**

* File: `signup.php`
* Fields (all required with regex validation in **JS** + **PHP**):

  * Email: must match email pattern.
  * Mobile: exactly 10 digits.
  * Full Name: first, middle, last, family — text only.
  * Password: min 8 chars, includes uppercase, lowercase, number, special char, no spaces.
  * Confirm Password: must match Password.
* Backend validation:

  * Use `filter_var()` for email.
  * Use regex for phone and password.
* Store:

  * Hash password with `password_hash()`.
  * Save record to `users` table.
* Redirect to `login.php` on success.

---

### **4. Login Page**

* File: `login.php`
* Validate:

  * Both fields filled.
  * Email format valid.
  * Password verified with `password_verify()`.
* Start session:

  * Store user’s `id`, `email`, `full_name`, `role`.
* Redirect:

  * If `role = User` → `welcome.php`
  * If `role = Admin` → `admin_dashboard.php`

---

### **5. Welcome Page**

* File: `welcome.php`
* Display:

  * User’s email and full name.
  * Static welcome message.
* Protect page with session check.

---

### **6. Admin Dashboard**

* File: `admin_dashboard.php`
* Display table:

  * ID | User Image | Name | Email | Date Created | Phone Number
* Features:

  * View all users.
  * Add new user (`admin_add.php`).
  * Edit user (`admin_edit.php`).
  * Delete user (`admin_delete.php`).
* Use **prepared statements** for CRUD.

---

### **7. Sessions & Logout**

* Store session data for logged-in users.
* Create `logout.php` to destroy session and redirect to landing page.

---

## 📦 Deliverables

* `index.php` – Landing page
* `signup.php` – Registration form with validation & DB insert
* `login.php` – Login form with validation & authentication
* `welcome.php` – User dashboard
* `admin_dashboard.php` – Admin panel
* `admin_add.php`, `admin_edit.php`, `admin_delete.php` – Admin CRUD
* `logout.php` – Logout functionality
* `config.php` – DB connection file
* SQL file (`php_advanced_auth.sql`) with table structure and sample Admin/User records

---

## 💡 Extra Tips

* Use **Bootstrap** for responsive styling.
* Apply **regex** for frontend JS validation and **PHP validation** for backend security.
* Always hash passwords with `password_hash()` and verify with `password_verify()`.
* Restrict admin pages to `role = 'Admin'` users only.
* Store uploaded user images in a dedicated `/uploads` folder.
