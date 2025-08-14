# 🗃️ Task 3: Advanced SQL (DDL & DML tasks)

## Modules Covered

1. Model6: DDL
2. Model7: DML
3. Model8: Data Querying Techniques

---
## **Excercise 1: School Management System Database**

### 🎯 Objectives

* Create a relational database for managing students, teachers, classes, and enrollments.
* Practice SQL DDL and DML commands: `CREATE`, `INSERT`, `UPDATE`, `DELETE`, and `SELECT`.
* Establish relationships between tables using primary and foreign keys.

---

### Steps

1. **Create the Database**

   * Name it `SchoolDB`.

2. **Create Tables**

   * `Students` (StudentID, FirstName, LastName, BirthDate, Email)
   * `Teachers` (TeacherID, FirstName, LastName, Email)
   * `Classes` (ClassID, ClassName, TeacherID – FK)
   * `Enrollments` (EnrollmentID, StudentID – FK, ClassID – FK, EnrollmentDate)

3. **Insert Sample Data**

   * Add at least 5 rows per table.

4. **Run SQL Operations**

   * `INSERT`: Add a new student.
   * `SELECT`: List all classes with teacher names.
   * `UPDATE`: Change email for TeacherID = 2.
   * `DELETE`: Remove enrollment for StudentID = 3.

---
### 📖 Query Hints for School Management System

```
-- School Database Tables

CREATE TABLE Students (
    StudentID INT PRIMARY KEY AUTO_INCREMENT,
    FirstName VARCHAR(50) NOT NULL,
    LastName VARCHAR(50) NOT NULL,
    BirthDate DATE,
    Email VARCHAR(100)
);

CREATE TABLE Teachers (
    TeacherID INT PRIMARY KEY AUTO_INCREMENT,
    FirstName VARCHAR(50) NOT NULL,
    LastName VARCHAR(50) NOT NULL,
    Email VARCHAR(100)
);

CREATE TABLE Classes (
    ClassID INT PRIMARY KEY AUTO_INCREMENT,
    ClassName VARCHAR(100) NOT NULL,
    TeacherID INT,
    FOREIGN KEY (TeacherID) REFERENCES Teachers(TeacherID)
);

CREATE TABLE Enrollments (
    EnrollmentID INT PRIMARY KEY AUTO_INCREMENT,
    StudentID INT,
    ClassID INT,
    EnrollmentDate DATE,
    FOREIGN KEY (StudentID) REFERENCES Students(StudentID),
    FOREIGN KEY (ClassID) REFERENCES Classes(ClassID)
);

```
# 📝 Data samples
```
-- Insert sample data for Students
INSERT INTO Students (FirstName, LastName, BirthDate, Email) VALUES
('Ali', 'Hassan', '2005-03-15', 'ali.hassan@email.com'),
('Sara', 'Omar', '2006-07-21', 'sara.omar@email.com'),
('Khalid', 'Nasser', '2004-12-01', 'khalid.nasser@email.com'),
('Lina', 'Ahmad', '2005-09-09', 'lina.ahmad@email.com'),
('Omar', 'Suleiman', '2006-01-19', 'omar.suleiman@email.com');

-- Insert sample data for Teachers
INSERT INTO Teachers (FirstName, LastName, Email) VALUES
('Mohammad', 'Saleh', 'm.saleh@school.com'),
('Fatima', 'Ali', 'f.ali@school.com'),
('Yousef', 'Khaled', 'y.khaled@school.com');

-- Insert sample data for Classes
INSERT INTO Classes (ClassName, TeacherID) VALUES
('Mathematics', 1),
('Science', 2),
('History', 3);

-- Insert sample data for Enrollments
INSERT INTO Enrollments (StudentID, ClassID, EnrollmentDate) VALUES
(1, 1, '2023-09-01'),
(2, 1, '2023-09-02'),
(3, 2, '2023-09-01'),
(4, 3, '2023-09-03'),
(5, 2, '2023-09-05');

```
---
### 📦 Deliverables

* SQL script (`schooldb.sql`) with table creation, inserts, and all queries.
* ER diagram showing relationships.
* Screenshot of output for each query.

---

### 💡 Extra Tips

* Use `JOIN` for retrieving class-teacher data.
* Validate data types (`DATE` for BirthDate, etc.).
* Use `ON DELETE CASCADE` for enrollments if a student is deleted.

---

## **Excercise 2: Library Database Operations**

### 🎯 Objectives

* Manage books, authors, members, and borrowed books.
* Apply `WHERE`, `ORDER BY`, aggregate functions, `LIKE`, `GROUP BY`, and `JOIN`.

---

### Steps

1. **Create Tables**

   * `Books` (BookID, Title, AuthorID – FK, Genre, Price, PublicationDate)
   * `Authors` (AuthorID, Name, Country)
   * `Members` (MemberID, FirstName, LastName, Email, JoinDate)
   * `BorrowedBooks` (BorrowID, BookID – FK, MemberID – FK, BorrowDate, ReturnDate)

2. **Insert Sample Data**

   * Fill enough records to make all queries meaningful.

3. **Run Queries**

   * `INSERT`: Add a book (“The Great Gatsby”).
   * `SELECT`: Books by AuthorID = 1.
   * `UPDATE`: Price of BookID = 2 to 20.99.
   * `DELETE`: Remove BookID = 3.
   * `WHERE`: Find all "Science Fiction" books.
   * `AND/OR/NOT`: Books in Fiction priced < 20 OR not by AuthorID = 2.
   * `ORDER BY`: Sort by PublicationDate DESC.
   * `MIN/MAX`: Get min and max prices.
   * `COUNT/AVG/SUM`: Book count, average price, total price.
   * `LIKE`: Titles starting with “The”.
   * `GROUP BY`: Count of books per genre.
   * `INNER JOIN`: Books with author names.

---

### 📦 Deliverables

* SQL script (`librarydb.sql`) with schema, inserts, and queries.
* Screenshots for at least 8 queries showing correct output.
* Short README explaining table relationships.

---
### 📖 Query Hints for Library Database
```
-- Library Database Tables

CREATE TABLE Authors (
    AuthorID INT PRIMARY KEY AUTO_INCREMENT,
    Name VARCHAR(100) NOT NULL,
    Country VARCHAR(50)
);

CREATE TABLE Books (
    BookID INT PRIMARY KEY AUTO_INCREMENT,
    Title VARCHAR(200) NOT NULL,
    AuthorID INT,
    Genre VARCHAR(50),
    Price DECIMAL(5,2),
    PublicationDate DATE,
    FOREIGN KEY (AuthorID) REFERENCES Authors(AuthorID)
);

CREATE TABLE Members (
    MemberID INT PRIMARY KEY AUTO_INCREMENT,
    FirstName VARCHAR(50) NOT NULL,
    LastName VARCHAR(50) NOT NULL,
    Email VARCHAR(100),
    JoinDate DATE
);

CREATE TABLE BorrowedBooks (
    BorrowID INT PRIMARY KEY AUTO_INCREMENT,
    BookID INT,
    MemberID INT,
    BorrowDate DATE,
    ReturnDate DATE,
    FOREIGN KEY (BookID) REFERENCES Books(BookID),
    FOREIGN KEY (MemberID) REFERENCES Members(MemberID)
);

```
# 📝 Data samples
```
-- Insert Authors
INSERT INTO Authors (Name, Country) VALUES
('F. Scott Fitzgerald', 'USA'),
('George Orwell', 'UK'),
('Isaac Asimov', 'Russia'),
('Agatha Christie', 'UK');

-- Insert Books
INSERT INTO Books (Title, AuthorID, Genre, Price, PublicationDate) VALUES
('The Great Gatsby', 1, 'Fiction', 15.99, '1925-04-10'),
('1984', 2, 'Science Fiction', 12.50, '1949-06-08'),
('Foundation', 3, 'Science Fiction', 18.75, '1951-06-01'),
('Murder on the Orient Express', 4, 'Mystery', 14.20, '1934-01-01'),
('Animal Farm', 2, 'Fiction', 9.99, '1945-08-17'),
('I, Robot', 3, 'Science Fiction', 16.50, '1950-12-02');

-- Insert Members
INSERT INTO Members (FirstName, LastName, Email, JoinDate) VALUES
('John', 'Doe', 'john.doe@example.com', '2022-12-15'),
('Jane', 'Smith', 'jane.smith@library.com', '2023-02-10'),
('Emily', 'Johnson', 'emily.j@example.com', '2023-03-05'),
('Michael', 'Brown', 'michael.b@library.com', '2023-04-12'),
('Sarah', 'Davis', 'sarah.d@example.com', '2023-06-21');

-- Insert BorrowedBooks
INSERT INTO BorrowedBooks (BookID, MemberID, BorrowDate, ReturnDate) VALUES
(1, 2, '2023-02-11', '2023-02-18'),
(2, 2, '2023-02-20', '2023-02-27'),
(3, 2, '2023-03-05', '2023-03-12'),
(4, 2, '2023-03-15', '2023-03-22'),
(5, 3, '2023-03-06', '2023-03-13'),
(6, 3, '2023-03-20', '2023-03-27'),
(1, 4, '2023-04-13', '2023-04-20'),
(2, 4, '2023-04-25', '2023-05-02'),
(3, 4, '2023-05-10', '2023-05-17'),
(4, 4, '2023-05-20', '2023-05-27'),
(5, 4, '2023-06-05', '2023-06-12'),
(6, 5, '2023-06-22', '2023-06-29');

```
---
### 💡 Extra Tips

* Use `DECIMAL(5,2)` for Price.
* Always test `WHERE` conditions before updates/deletes.
* Remember `GROUP BY` needs an aggregate function.

---

## **Excercise 3: Member Borrowing Analysis**

### 🎯 Objectives

* Use filtering, aggregation, and sorting to analyze borrowing patterns.
* Apply multiple conditions in SQL queries.

---

### Steps

1. **Given Tables**: `Members`, `BorrowedBooks` (data provided in task).
2. **Query Requirements**:

   * List members who:

     * Joined after `2023-01-01`.
     * Borrowed more than 3 books.
     * Do **not** have emails ending with `@example.com`.
   * Sort results by `LastName` ASC.

---

### 📦 Deliverables

* SQL query (`member_analysis.sql`) file.
* Screenshot showing result set.
* Short explanation of filtering logic.

---

### 💡 Extra Tips

* Use `COUNT()` with `GROUP BY` to check borrow count per member.
* Apply `HAVING` after `GROUP BY` for conditions on aggregates.
* Use `NOT LIKE '%@example.com'` for email filtering.

---

## **Excercise 4: Advanced Library Queries**

### 🎯 Objectives

* Work with aggregate functions, pattern matching, grouping, and joins.
* Focus on analyzing borrowed books based on member details.

---

### Steps

1. **Use Provided Books & Members Data**.
2. **Run Queries**:

   * `MIN/MAX`: Prices of books borrowed by members joined after `2023-01-01`.
   * `COUNT/AVG/SUM`: Borrow count, average price, total price for those members.
   * `LIKE`: Members whose last name starts with “J”.
   * `GROUP BY`: Books borrowed count per member.
   * `INNER JOIN`: Members with titles of borrowed books.

---

### 📦 Deliverables

* SQL script (`advanced_library.sql`) with all queries.
* Screenshots for each query’s result.
* Brief note on insights from the queries.

---

### 💡 Extra Tips

* Use subqueries or joins to filter borrowed books for certain members.
* Test joins to avoid duplicate rows.
* Be consistent with date comparisons (`YYYY-MM-DD`).
