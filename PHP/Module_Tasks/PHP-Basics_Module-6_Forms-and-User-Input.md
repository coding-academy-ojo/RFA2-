# 🐘 Module 6: Forms and User Input

## 🎯 Objectives

* Understand how HTML forms work with PHP.
* Learn the difference between **`$_GET`** and **`$_POST`**.
* Perform **server-side validation**.
* Handle different types of form inputs (text, password, email, radio, checkbox, select, textarea).
* Give user-friendly feedback after submission.

---

### **Task 1 – Simple Feedback Form**

Create an HTML form that collects:

* Name
* Email
* Feedback message
  When submitted, the PHP script should:
* Display the submitted values back to the user.
* Ensure **no field is empty**.

---

### **Task 2 – Login Form with Validation**

Create a login form with:

* Username
* Password
  In the PHP script:
* If username = `admin` and password = `1234`, display `"Welcome Admin"`.
* Otherwise, display `"Invalid credentials"`.

---

### **Task 3 – Calculator Form**

Make a form that:

* Takes two numbers and an operator (+, -, ×, ÷)
  PHP should:
* Calculate and display the result.
* Handle division by zero with a friendly message.

---

### **Task 4 – Registration Form with Validation**

Create a form with:

* Name
* Email
* Password
* Confirm Password
  Requirements:
* Password must be **at least 6 characters**.
* Email must be valid format.
* Password and Confirm Password must match.


---
## 📦 **Deliverables**

By the end of this module, you will submit:

* PHP scripts that handle **form submission** using `$_GET` and `$_POST`.
* At least **4 different form examples** (login, feedback, calculator, registration).
* Demonstrations of **input validation** .

---
## 💡 **Tips**

* Always **validate** on the server side (client-side validation can be bypassed).
* Use `htmlspecialchars()` to prevent XSS.
* Use `filter_var($email, FILTER_VALIDATE_EMAIL)` to check email validity.
* `$_GET` is visible in the URL, **never** use it for passwords.
* Keep error messages clear for the user.

---

## 🚀 **Extra Challenge**

* Create a **multi-step form** (Page 1 → Page 2 → Page 3) where:

  * Data from previous pages is passed along.
  * At the final step, all data is displayed in a summary table.
* Add a **file upload field** that only accepts `.jpg` or `.png` files, max size **2MB**.
* Store submitted form data in a **CSV file** for later review.
