# 🗃️ Task 1: Introduction to Databases & Basic SQL Operations

## Modules Covered

1. Model1: Core Concepts – Introduction to Databases and RDBMS
2. Model2: Database Models
3. Model3: Relational Model
4. Model4: Normalization
5. Model5: Introduction to SQL (Structured Query Language)

---

## 🎯 Objectives

Design and implement a relational database for a company using MySQL.
You will apply fundamental database concepts (RDBMS, data models, normalization) and practice creating databases, tables, relationships, inserting data, and writing basic SQL queries.

---

## Steps

### 1. **Create the Database**

* Create a database named `CompanyDB`.

### 2. **Create Tables**

* Create the following tables with the specified columns and constraints:

**Employees**

* `ID` (Primary Key)
* `EmployeeName`
* `Salary`
* `PhoneNumber`
* `DepartmentID` (Foreign Key referencing `Departments.ID`)
* `City`

**Departments**

* `ID` (Primary Key)
* `DepartmentName`

### 3. **Insert Data**

* Insert **at least 5 records** into each table.
* Ensure data follows **normalization principles** (no duplicate or redundant info).

### 4. **Write SQL Queries**

Perform the following tasks:

1. Select all employee data.
2. Order employees by salary in **descending** order.
3. Get the employee with the **highest salary**.
4. Get the employee with the **lowest salary**.
5. Count the total number of employees.
6. Find employees with a salary of **500**.
7. Find employees with a salary **greater than 500**.
8. Find employees with salary greater than 500 **and** city = 'Salt'.
9. Calculate the **sum** of all salaries.
10. Find employees whose names **start** with 'A'.
11. Find employees whose names **end** with 'A'.
12. Find employees in cities **'Salt', 'Amman', 'Aqaba'**.
13. Find employees with salary **between 300 and 500**.
14. Update the salary of any employee.
15. Get all **unique cities** where employees are located.
16. Get **unique cities** and **count** how many employees are in each.
17. Ensure a **foreign key relationship** exists between `Employees` and `Departments`.

---

## 📦 Deliverables

1. **SQL Script File** (`companydb.sql`) containing:

   * Database creation
   * Table creation with constraints
   * Insert statements
   * All queries from Step 4
2. **ER Diagram** (image or PDF) showing the relationship between tables.
3. **Screenshots** of:

   * Tables after inserting data
   * Outputs for at least 5 of the SQL queries.
4. A short **README.md** explaining:

   * Database structure
   * Chosen data types
   * How normalization was applied.
