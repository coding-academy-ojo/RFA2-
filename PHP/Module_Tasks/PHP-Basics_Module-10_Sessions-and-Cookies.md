# 🐘 Module 10: Sessions and Cookies

## 🎯 Objectives

By the end of this module, students will be able to:

* Understand the concept of sessions and cookies in PHP.
* Initialize and manage PHP sessions to store and retrieve user data.
* Modify and destroy session data securely.
* Set, retrieve, and delete cookies with proper expiration handling.

---
### 📝 **Task 1: Start a PHP Session**
  1. Create a PHP script `session_start.php`.
  2. Start a session using `session_start()`.
  3. Store at least 2 variables in the session (e.g., `username` and `role`).
  4. Display the stored session data on the page.

---

### 📝 **Task 2: Retrieve and Modify Session Data**
  1. Create `session_modify.php`.
  2. Retrieve session variables from `session_start.php`.
  3. Update one of the session variables (e.g., change `role`).
  4. Display the updated session data.
  
---

### 📝 **Task 3: Destroy a Session**
  1. Create `session_destroy.php`.
  2. Destroy the current session using `session_destroy()`.
  3. Try accessing session variables after destruction and show they are cleared.

---

### 📝 **Task 4: Set and Retrieve Cookies**
  1. Create `cookie_set.php`.
  2. Set at least 2 cookies (e.g., `user` and `theme`) with expiration of 1 week.
  3. Display a message confirming cookies are set.

---

### 📝 **Task 5: Read and Delete Cookies**
  1. Create `cookie_read_delete.php`.
  2. Retrieve cookies set in Task 4 and display their values.
  3. Delete one cookie using `setcookie()` with a past expiration date.
  4. Show updated cookie list after deletion.

---

💡 **Extra Challenge Tasks**
  1. Create a login form (`login.php`) storing username in session.
  2. Store a “remember me” preference in a cookie.
  3. On next visit, auto-fill the username from the cookie and maintain session login state.

---

### 📦 Deliverables

* `index.php` with:

  * Simple PHP output
  * PHP embedded inside HTML
  * At least one PHP variable and function call
* A screenshot of the page in the browser.
