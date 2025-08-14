# 🗃️ Task 6: SmartBuy Database – SQL Joins & Aggregations

## Modules Covered

* Table Relationships (1\:N, N\:N)
* Joins (INNER, LEFT, RIGHT, FULL OUTER)
* Aggregations & GROUP BY
* Conditional Logic with CASE
* UNION Queries

---

## 🎯 Objectives

Query the SmartBuy database to retrieve customer, order, product, employee, and project data using different join types, aggregations, and filtering.

---

## Steps

### **1. Create Tables & Insert Data**

Use the provided SQL in the task description to create:

* `customers`
* `orders`
* `products`
* `order_details`
* `employees`
* `departments`
* `projects`
* `employee_projects`

---

### **2. Write SQL Queries**

1. Customers + orders (INNER JOIN).
2. Products + order details, include products with no orders (LEFT JOIN + `IS NULL`).
3. Employees + departments, include departments with no employees (RIGHT JOIN).
4. Total sales per product (SUM + GROUP BY).
5. Orders with customer names, product names, and quantities (Multiple JOINs).
6. Customers with > 5 orders (COUNT + HAVING).
7. Employees + projects (FULL OUTER JOIN with COALESCE).
8. Active & inactive customers with orders, separated by status (UNION).
9. Orders with status: Shipped, Pending, or Canceled (CASE logic).

---

## 📦 Deliverables

* `smartbuy_queries.sql` file with:

  * All 9 queries
  * Comments explaining logic
* Screenshots of at least 5 query outputs.
* README explaining:

  * Relationship diagram
  * Which join type was used for each task

---

## 💡 Extra Tip

* For FULL OUTER JOIN in MySQL, simulate using `UNION` of LEFT + RIGHT JOIN.
