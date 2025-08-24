# Task 7: PHP Advanced – Admin Dashboard with Employee Management
<img width="770" height="503" alt="image" src="https://github.com/user-attachments/assets/4c49d96a-965e-48ed-a55c-d081292a716e" />

## 🎯 Goal

Build a professional **Admin Dashboard** in PHP + MySQL with **cards, CRUD operations, salary calculations, and search functionality**.

---

## Steps

### **1. Database Setup**

```sql
CREATE DATABASE company_db;

USE company_db;

CREATE TABLE employees (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    salary DECIMAL(10,2) NOT NULL,
    offdays INT DEFAULT 0
);
```

---

### **2. Admin Dashboard (index.php)**

* Show **cards** with real-time values:

  * Highest Salary
  * Lowest Salary
  * Sum of Salaries
  * Total Number of Employees
* Display **Employee Table** with full CRUD (Create, Read, Update, Delete).
* Bootstrap cards + table for styling.

---

### **3. CRUD Operations for Employees**

* `create.php` → Add new employee
* `read.php` → View all employees (table with actions)
* `update.php` → Edit employee details
* `delete.php` → Delete employee by ID

---

### **4. Salary Update Page (update\_salary.php)**

* Update salary for **a single employee** or **all employees**.
* Options:

  * Increase by fixed amount or percentage
  * Decrease by fixed amount or percentage

---

### **5. Salary Calculation Page (calculate\_salary.php)**

* Formula:

  ```
  Net Salary = Salary – (Offdays × (Salary / 30)) 
  ```
* Show calculation in a styled result card.

---

### **6. Search Functionality (search.php)**

* Search employees by:

  * Employee ID
  * Employee Name (partial match)
* Display results in table format.

---

## 📦 Deliverables

* `config.php` → Database connection (PDO or MySQLi)
* `index.php` → Dashboard with salary/statistics cards + employee table
* `create.php` → Add employee form
* `read.php` → Employee table with actions
* `update.php` → Update employee data
* `delete.php` → Remove employee
* `update_salary.php` → Update employee/all salaries
* `calculate_salary.php` → Salary calculation based on offdays
* `search.php` → Employee search page
* SQL file (`company_db.sql`) with schema + sample data
* `README.md` → Explaining setup, usage, and features

---

## 💡 Extra Tips

* Use **Bootstrap 5** or **AdminLTE** for a professional UI.
* Protect all pages with **login & session checks**.
* Use **prepared statements** to prevent SQL injection.
* Add **confirmation modals** before delete operations.
* Extend system with **pagination** for employee list.

---

👉 Do you want me to also **generate the starter SQL + PHP code for the cards and CRUD** so you’ll have a ready-to-run demo, or should I just keep it as a structured GitHub task description like this?
