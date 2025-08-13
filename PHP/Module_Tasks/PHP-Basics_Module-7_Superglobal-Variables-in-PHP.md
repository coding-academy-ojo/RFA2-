# 🐘 Module 7: Super Global Variables in PHP

## 🎯 Objectives

By completing these exercises, you will:

* Gain hands-on experience with PHP’s superglobal variables (`$_GET`, `$_POST`, `$_SERVER`, `$_REQUEST`, `$_COOKIE`, `$_SESSION`, `$_FILES`, `$_ENV`).
* Learn how to capture, process, and validate user input.
* Explore basic web application features like forms, redirection, cookies, sessions, and visitor counters.
* Understand how to track and store data across multiple page requests.

---

## 📚 **Exercises**

### **1. Form Method Detector**

**Task:**

* Create a form with email and password fields.
* In the action page, detect if the data is sent via GET or POST using `$_SERVER['REQUEST_METHOD']`.
* Display the method used and the submitted data.

---

### **2. Simple Search Redirect**

**Task:**

* Create a form with a single input field for a URL and a "GO" button.
* When the user clicks "GO", redirect them to the entered URL using `header("Location: ...")`.

---

### **3. Basic Calculator**

**Task:**

* Create a calculator form with two number inputs and a dropdown for operations (+, -, \*, /).
* Submit the form and display the result using the selected operation.

---

### **4. To-Do List Application**

**Task:**

* Create a to-do list where users can add tasks via a form.
* Store the tasks in a session (`$_SESSION`).
* Allow deleting tasks by clicking a "Delete" button next to each task.

---

### **5. Project & Script Info**

**Task:**

* Display the **project name** and **current script filename** using `$_SERVER['SCRIPT_NAME']` and `basename(__FILE__)`.

---

### **6. Page Requested Time**

**Task:**

* Display the date and time when the page was requested using `$_SERVER['REQUEST_TIME']`.

---

### **7. Page Refresh Counter**

**Task:**

* Create a counter that increments every time the page is refreshed using a session variable.

---

### **8. Visitor Counter (Persistent)**

**Task:**

* Create a counter that tracks total unique visitors using cookies (`$_COOKIE`).

---

### **9. Cookie Creation, Retrieval & Deletion**

**Task:**

* Create a cookie with:

  * Name
  * Value
  * Expiry time
  * Path
  * Domain
  * Secure flag
  * HttpOnly flag
* Display all cookies set in the browser using `$_COOKIE`.
* Provide a button to delete the cookie.

---

### **10. File Upload Handler**

**Task:**

* Create a form with a file upload field.
* Handle the upload using `$_FILES`.
* Display file information such as name, size, and type.

---

### **11. Server Information Page** *(Extra)*

**Task:**

* Create a page that displays server info using:

  * `$_SERVER['HTTP_USER_AGENT']` – Browser info
  * `$_SERVER['SERVER_NAME']` – Server hostname
  * `$_SERVER['REMOTE_ADDR']` – Visitor’s IP address

---

### **12. Environment Variables Reader** *(Extra)*

**Task:**

* Display environment variables from `$_ENV` (e.g., system paths, OS details).

---

## 📦 **Deliverables**

* A folder containing each exercise’s PHP files.
* Each exercise should be tested for both functionality and security.
* A short README.md explaining the purpose of each script.
---
## 💡 **Tips**

* Always sanitize and validate user input before using it.
* Use `htmlspecialchars()` to prevent XSS attacks when displaying user-submitted content.
* Remember that `$_GET` sends data via the URL (less secure), while `$_POST` sends it in the request body.
* Cookies are stored on the client-side; Sessions are stored server-side.
* Use `isset()` and `empty()` to check if values are set.
* Use `$_SERVER['REQUEST_METHOD']` to detect whether a form was submitted via GET or POST.
