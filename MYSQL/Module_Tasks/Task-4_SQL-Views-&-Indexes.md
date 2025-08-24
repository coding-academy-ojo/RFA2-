# 🗃️ Task 4: Creating and Using Views & Indexes in MySQL

## Modules Covered

* Module 9: Views and Indexes
* Query Optimization Basics
* Data Retrieval and Management

---

## 🎯 Objectives

Learn how to create, modify, and use **views** for simplified data retrieval, and how to create **indexes** to improve query performance in MySQL.

---

## Steps

### **1. Create the Database**

* Use an existing database (e.g., `CompanyDB`) or create a new one named `ViewIndexDB`.

---

### **2. Prepare Sample Tables**

Create two tables with sample data:

```sql
CREATE TABLE Employees (
    emp_id INT PRIMARY KEY AUTO_INCREMENT,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    department VARCHAR(50),
    salary DECIMAL(10,2),
    hire_date DATE
);

CREATE TABLE Departments (
    dept_id INT PRIMARY KEY AUTO_INCREMENT,
    department_name VARCHAR(50),
    location VARCHAR(50)
);
```

Insert at least **8 employees** across different departments, and **3 departments**.

---

### **3. Create Views**

1. **Basic View** – Create a view `employee_summary` showing `first_name`, `last_name`, `department`, and `salary`.
2. **Filtered View** – Create a view `high_salary_employees` showing employees with salary > 5000.
3. **Join View** – Create a view `employee_department_info` that joins `Employees` and `Departments` to show each employee’s department location.
4. Query data from each view.

---

### **4. Create Indexes**

1. Create an index on `salary` in the `Employees` table.
2. Create a composite index on `(department, salary)` in `Employees`.
3. Use `EXPLAIN` to compare query performance before and after indexing.

---

### **5. Modify & Drop**

* Modify the `high_salary_employees` view to include `hire_date`.
* Drop one of the indexes and one of the views.

---

## 📦 Deliverables

* **SQL Script File** (`views_indexes.sql`) containing:

  * Table creation.
  * Insert statements.
  * All `CREATE VIEW`, `ALTER VIEW`, `DROP VIEW` commands.
  * All `CREATE INDEX`, `DROP INDEX` commands.
  * Sample queries using the views and indexed columns.
* **Screenshots** of:

  * View query results.
  * `EXPLAIN` output before and after indexing.
* **README.md** summarizing:

  * What views are and when to use them.
  * What indexes are and how they improve performance.

---

## 💡 Extra Tips

* Use views to simplify complex joins for regular queries.
* Index columns that are frequently used in `WHERE`, `ORDER BY`, and `JOIN` clauses.
* Avoid indexing every column; indexes take extra storage and slow down inserts/updates.
* Use `SHOW INDEX FROM table_name;` to check existing indexes.
