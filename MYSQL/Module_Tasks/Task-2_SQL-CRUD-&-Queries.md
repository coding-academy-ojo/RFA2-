# 🗃️ Task 2: School Management System – SQL CRUD & Queries

## Modules Covered

* Core Concepts – Introduction to Databases and RDBMS
* Relational Model
* Data Definition Language (DDL)
* Data Manipulation Language (DML)
* Querying Data in SQL

---

## 🎯 Objectives

Create and manage a **School Management System** in MySQL (phpMyAdmin) that handles students, teachers, courses, and enrollments.
You will design the database schema, insert sample data, and run SQL queries to retrieve, update, and delete records.

---

## Steps

### **1. Create the Database**

* Name it `SchoolManagement`.

### **2. Create the Tables**

```sql
CREATE TABLE Students (
    student_id INT PRIMARY KEY AUTO_INCREMENT,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    date_of_birth DATE,
    gender CHAR(1),
    enrollment_date DATE
);

CREATE TABLE Teachers (
    teacher_id INT PRIMARY KEY AUTO_INCREMENT,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    hire_date DATE,
    subject VARCHAR(100)
);

CREATE TABLE Courses (
    course_id INT PRIMARY KEY AUTO_INCREMENT,
    course_name VARCHAR(100) NOT NULL,
    teacher_id INT,
    FOREIGN KEY (teacher_id) REFERENCES Teachers(teacher_id)
);

CREATE TABLE Enrollments (
    enrollment_id INT PRIMARY KEY AUTO_INCREMENT,
    student_id INT,
    course_id INT,
    enrollment_date DATE,
    FOREIGN KEY (student_id) REFERENCES Students(student_id),
    FOREIGN KEY (course_id) REFERENCES Courses(course_id)
);
```

---

### **3. Insert Sample Data**

Insert at least **5 students**, **3 teachers**, **3 courses**, and corresponding enrollments so all queries will produce meaningful results.

---

### **4. Complete the Tasks**

Run SQL queries for:

1. **Insert** new records into `Students`.
2. **Select** all students enrolled after `'2020-01-01'`.
3. **Update** last name of student with `student_id = 1`.
4. **Delete** student with `student_id = 1`.
5. Select students who are **female** (`gender = 'F'`).
6. Select students who are **male OR enrolled after 2020**.
7. Select all students **ordered by last name**.
8. Find **earliest** and **latest** enrollment dates.
9. Count total number of students.
10. Find students whose first name starts with `'J'`.
11. **Group** students by gender and count each group.
12. Select students **with the courses** they are enrolled in (use `JOIN`).

---

## 📦 Deliverables

* **SQL Script File** (`school_management.sql`) containing:

  * All `CREATE TABLE` statements.
  * All `INSERT` statements.
  * All queries for the 12 tasks.
* **ER Diagram** showing relationships between tables.
* **Screenshots** of:

  * Sample data in each table.
  * Output for at least 5 of the queries.
* **README.md** explaining:

  * Database structure.
  * How to import and run the script.

---

## 💡 Extra Tips

* Use `AUTO_INCREMENT` for all primary keys.
* Always test `WHERE` clauses before `UPDATE` or `DELETE`.
* Use `JOIN` instead of subqueries for Task 12 to combine student and course info.
* Keep dates in `YYYY-MM-DD` format for MySQL compatibility.
