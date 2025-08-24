# Task 6: Advanced PHP APIs – School Management System

## Modules Covered

* Module 5: Connecting PHP with MySQL
* Module 6: CRUD Operations with PHP & MySQL
* Module 8: Authentication and API Security
* Module 9: Creating a Database Class in PHP
* Module 14: Advanced CRUD Features (MySQLi + OOP)
* REST API Development with PHP

---

## 🎯 Goal

Build a **School Management System** with **CRUD operations** and a full set of **REST APIs** in PHP. Test the APIs using Postman and expand the database to handle Students, Teachers, Subjects, and Exams with proper relationships.

---

## Steps

### **Task 1: CRUD Operations for Students**

1. **Database Setup**

   ```sql
   CREATE DATABASE school_management;

   USE school_management;

   CREATE TABLE students (
       student_id INT AUTO_INCREMENT PRIMARY KEY,
       name VARCHAR(100) NOT NULL,
       class VARCHAR(50),
       date_of_birth DATE,
       address VARCHAR(255),
       contact_info VARCHAR(100)
   );
   ```

2. **API Endpoints (JSON Input/Output)**

   * Create Student → `POST /api/students`
   * Read Students → `GET /api/students`
   * Read Single Student → `GET /api/students/:id`
   * Update Student → `PUT /api/students/:id`
   * Delete Student → `DELETE /api/students/:id`

3. **Test with Postman**

   * Create a Postman collection with requests for all CRUD endpoints.

---

### **Task 2: API Endpoints for Students**

* **Create Student (POST)**
  Endpoint: `/api/students`
  Request Body: `{ "name": "...", "class": "...", "date_of_birth": "...", "address": "...", "contact_info": "..." }`
  Response: JSON with new student’s details

* **Update Student (PUT)**
  Endpoint: `/api/students/:studentId`
  Request Body: Partial/Full JSON fields
  Response: JSON with updated student

* **Delete Student (DELETE)**
  Endpoint: `/api/students/:studentId`
  Response: `{ "message": "Student deleted successfully" }`

---

### **Task 3: Expand Database (Teachers, Subjects, Exams)**

1. **New Tables**

   ```sql
   CREATE TABLE teachers (
       teacher_id INT AUTO_INCREMENT PRIMARY KEY,
       name VARCHAR(100) NOT NULL,
       subject_id INT UNIQUE,
       contact_info VARCHAR(100)
   );

   CREATE TABLE subjects (
       subject_id INT AUTO_INCREMENT PRIMARY KEY,
       name VARCHAR(100) NOT NULL,
       description TEXT
   );

   CREATE TABLE exams (
       exam_id INT AUTO_INCREMENT PRIMARY KEY,
       subject_id INT,
       exam_date DATE,
       max_score INT,
       FOREIGN KEY (subject_id) REFERENCES subjects(subject_id)
   );

   -- Many-to-Many: Students ↔ Subjects
   CREATE TABLE student_subjects (
       student_id INT,
       subject_id INT,
       PRIMARY KEY (student_id, subject_id),
       FOREIGN KEY (student_id) REFERENCES students(student_id),
       FOREIGN KEY (subject_id) REFERENCES subjects(subject_id)
   );
   ```

2. **Relationships**

   * Students ↔ Subjects: Many-to-Many (`student_subjects`)
   * Teachers ↔ Subjects: One-to-One
   * Subjects ↔ Exams: One-to-Many

---

### **Task 3: API Endpoints for Teachers, Subjects, Exams**

* Teachers:

  * Create → `POST /api/teachers`
  * Get All → `GET /api/teachers`
  * Get by ID → `GET /api/teachers/:teacherId`

* Subjects:

  * Create → `POST /api/subjects`
  * Get All → `GET /api/subjects`
  * Get by ID → `GET /api/subjects/:subjectId`

* Exams:

  * Create → `POST /api/exams`
  * Get All → `GET /api/exams`
  * Get by ID → `GET /api/exams/:examId`

---

### **Task 4: Advanced Customer Requests APIs**

1. **Retrieve a Student's Subjects (GET)**
   Endpoint: `/api/students/:id/subjects`

2. **Retrieve a Subject's Students (GET)**
   Endpoint: `/api/subjects/:id/students`

3. **Register Students in Subjects (POST)**
   Endpoint: `/api/students/:id/subjects`
   Request Body: `{ "subjects": [1,2,3] }`

4. **Retrieve a Student’s Exams (GET)**
   Endpoint: `/api/students/:id/exams`

5. **Retrieve a Subject’s Exams (GET)**
   Endpoint: `/api/subjects/:id/exams`

6. **Update Exam (PUT)**
   Endpoint: `/api/exams/:id`
   Request Body: `{ "exam_date": "...", "max_score": ... }`

---

## 📦 Deliverables

* `config.php` – Database connection
* `students.php` – CRUD API for students
* `teachers.php` – CRUD API for teachers
* `subjects.php` – CRUD API for subjects
* `exams.php` – CRUD API for exams
* `student_subjects.php` – Many-to-many relation APIs
* SQL file (`school_management.sql`) with all tables and sample data
* Postman collection (`SchoolAPI.postman_collection.json`)

---

## 💡 Extra Tips

* Always set **headers**:

  ```php
  header("Content-Type: application/json");
  ```
* Use **http\_response\_code()** for proper API responses (`200`, `201`, `400`, `404`, `500`).
* Use **prepared statements (PDO/MySQLi)** to prevent SQL injection.
* Use Postman for testing every endpoint with **valid & invalid** data.
* Document endpoints in your `README.md` so others can easily test them.
