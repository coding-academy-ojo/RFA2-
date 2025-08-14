# 🐘 + 🗃️ Task: PHP CRUD Application – Employee Management System

## Modules Covered

* Module 9: Creating a Database Class in PHP
* Module 10: PHP CRUD – Create Operation (MySQLi + OOP)
* Module 11: PHP CRUD – Read Operation (MySQLi + OOP)
* Module 12: PHP CRUD – Update Operation (MySQLi + OOP)
* Module 13: PHP CRUD – Delete Operation (MySQLi + OOP)
* Module 14: Advanced CRUD Features (MySQLi + OOP)

---

## 🎯 Objectives

Build a small **PHP + MySQL** web application to manage employees with full **CRUD functionality** (Create, Read, Update, Delete). The system will have a landing page to view employees, a form to add new employees, and pages to update or delete records.

---

## Steps

### **1. Create the Database**

```sql
CREATE DATABASE company_db;

USE company_db;

CREATE TABLE Employees (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    address VARCHAR(255),
    salary DECIMAL(10, 2)
);
```

---

### **2. Create the Config File**

* File: `config.php`
* Contains the database connection using MySQLi or PDO.
* Example:

```php
<?php
$servername = "localhost";
$username = "root";
$password = "";
$dbname = "company_db";

$conn = new mysqli($servername, $username, $password, $dbname);

if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}
?>
```

---

### **3. View Employees Page (Landing Page)**

* File: `index.php`
* Display all employee records in a **table/grid**.
* Each row has:

  * View button → `read.php?id=...`
  * Edit button → `update.php?id=...`
  * Delete button → `delete.php?id=...`
* Add **"Create Employee"** button linking to `create.php`.

---

### **4. Create Employee Page**

* File: `create.php`
* Form with fields: Name, Address, Salary.
* On submit, insert new employee record into the database.
* Redirect back to `index.php` after successful insertion.

---

### **5. Read Employee Page**

* File: `read.php`
* Retrieve a single employee by `id`.
* Display details in a simple layout (no editing).

---

### **6. Update Employee Page**

* File: `update.php`
* Pre-fill form with employee’s existing data.
* On submit, update the record in the database.
* Redirect to `index.php` after update.

---

### **7. Delete Employee Page**

* File: `delete.php`
* Ask for confirmation before deleting.
* Delete employee record by `id`.
* Redirect to `index.php` after deletion.

---

## 📦 Deliverables

* `config.php` (Database connection)
* `index.php` (View employees)
* `create.php` (Add employee)
* `read.php` (View details)
* `update.php` (Edit employee)
* `delete.php` (Remove employee)
* SQL file (`employees.sql`) with table structure and some sample data.

---

## 💡 Extra Tips

* Use **prepared statements** to prevent SQL injection.
* Add **basic form validation** before inserting or updating data.
* Style the table and forms using simple CSS or Bootstrap.
* For the Delete page, use a confirmation prompt in PHP (`confirm()` function).
