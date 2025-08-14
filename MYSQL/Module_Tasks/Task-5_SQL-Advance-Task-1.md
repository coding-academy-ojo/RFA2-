# 🗃️ Task 5: Online Bookstore Sales Dashboard Information – SQL Analysis

## Modules Covered

* Querying Data (SELECT, WHERE, ORDER BY)
* Aggregate Functions (COUNT, SUM, MAX, MIN, AVG)
* GROUP BY & HAVING
* Subqueries & Joins
* Advanced Filtering & Analysis

---

## 🎯 Objectives

Analyze 15 days of sales contest data for an online bookstore. Use SQL to produce insights such as daily sales, top-selling books, sales trends, and performance summaries.

---

## Steps

### **1. Create Tables**

```sql
CREATE TABLE Books (
    book_id INT PRIMARY KEY,
    title VARCHAR(200)
);

CREATE TABLE Sales (
    sale_id INT PRIMARY KEY,
    sale_date DATE,
    book_id INT,
    quantity INT,
    FOREIGN KEY (book_id) REFERENCES Books(book_id)
);
```

### **2. Insert Sample Data**

* Insert at least **10 books** into `Books`.
* Insert **15 days** of sales data into `Sales` covering `2024-04-01` to `2024-04-15`.

### **3. Write SQL Queries**

1. List all sales by date.
2. Count **unique books sold** each day.
3. Find **book with max sales each day** (lowest `book_id` if tie).
4. Summary of total sales and unique books sold.
5. Calculate **daily sales rate** = books sold ÷ total available books.
6. Identify sales peaks and dips.
7. Books sold **every day** of the contest.
8. Number of days each book was sold.
9. Sales count for each book each day.
10. Highest quantity sold per day.
11. Books with multiple sales in a day.
12. Books with sales < 5 copies.
13. Final contest summary: total sales, unique books, highest-selling book.

---

## 📦 Deliverables

* `bookstore_contest.sql` file with:

  * Table creation
  * Sample data
  * All queries
* Screenshots of at least 6 key query results.
* Short README with a **sales trend chart** (optional, generated from query results).

---

## 💡 Extra Tips

* Use `ROW_NUMBER()` or `RANK()` for daily top sellers.
* Use `EXISTS` or `HAVING COUNT()` for “sold every day” logic.
* Use `CASE` for sales rate classifications (e.g., high/low).
