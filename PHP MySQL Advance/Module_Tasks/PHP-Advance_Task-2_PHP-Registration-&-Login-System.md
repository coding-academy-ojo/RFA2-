# 🐘 + 🗃️ Task 1: PHP Registration & Login System

## Modules Covered

* Module 1: Introduction to PHP & MySQL Integration
* Module 5: Connecting PHP with MySQL
* Module 6: CRUD Operations – Create & Read
* Module 8: Authentication and Login System

---

## 🎯 Objectives

Create a **registration** and **login** system in PHP with MySQL integration. Validate user inputs, securely store credentials, and authenticate users against stored data.

---

## Steps

### **1. Create the Database**

```sql
CREATE DATABASE user_auth;

USE user_auth;

CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL
);
```

---

### **2. Registration Page**

* File: `register.php`
* Form fields:

  * Name (required, text)
  * Email (required, email)
  * Password (required, password)
  * Confirm Password (required, password)
* PHP validation:

  * All fields filled
  * Email format valid (`filter_var($email, FILTER_VALIDATE_EMAIL)`)
  * Passwords match
  * Password meets criteria (e.g., min 6 characters)
* Store:

  * Hash password using `password_hash()`
  * Insert into database using **prepared statements**
* On success:

  * Redirect to `login.php` with a success message

---

### **3. Login Page**

* File: `login.php`
* Form fields:

  * Email (required, email)
  * Password (required, password)
* PHP validation:

  * All fields filled
  * Email format valid
  * Check credentials:

    * Retrieve hashed password from DB
    * Verify with `password_verify()`
* On success:

  * Start a session (`$_SESSION['user_id']`)
  * Redirect to a dashboard or welcome page
* On failure:

  * Show an error message

---

### **4. Config File**

* File: `config.php`
* Central DB connection using MySQLi or PDO
* Include in both `register.php` and `login.php`

---

## 📦 Deliverables

* `config.php` (DB connection)
* `register.php` (registration form + PHP validation + DB insert)
* `login.php` (login form + authentication logic)
* SQL file (`users.sql`) with table structure and sample user
* Optional: `dashboard.php` to display a welcome message after login

---

## 💡 Extra Tips

* Always **hash passwords** — never store them as plain text.
* Use **prepared statements** to prevent SQL injection.
* Use session management to persist login state.
* Add password complexity checks for better security.
* Display meaningful error messages near the form fields.
Do you want me to prepare that?

