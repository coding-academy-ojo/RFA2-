Okay, here is the Laravel Roadmap Beginner Level Challenge presented in a modern Notion-style format:

---

# 🚀 **Laravel Roadmap: Beginner Level Challenge**

*Your First Step into Full-Stack Laravel Development*

---

## 🎯 **Mission Objective**

Implement a **Simple Personal Blog** using **Laravel**. This task focuses on applying core Laravel concepts. You'll start with an empty repository and submit your solution via a **Pull Request (PR)** for review.

---

## 📝 **Core Requirements**

### 🖥️ **Essential Pages**

1.  **Homepage:** A list view of all blog articles.
2.  **Article Page:** A detailed view for a single article.
3.  **Static Page:** An "About Me" (or similar) page with static content.

### 🔐 **Author Admin Panel**

*   Implement **Login** (Registration is *not* required).
*   Authenticated authors can **Manage**:
    *   **Categories** (Create, Update, Delete)
    *   **Tags** (Create, Update, Delete)
    *   **Articles** (Create, Update, Delete)

> 💡 **Starter Kit:** Use **Laravel Breeze (Tailwind)** or your preferred auth starter. Design is secondary; functionality is key.

---

## 🗃️ **Database Blueprint**

### **Entities & Fields**

*   **Article**
    *   `title` *(string, required)*
    *   `full_text` *(text, required)*
    *   `image` *(string, optional - for uploaded image path)*
*   **Category**
    *   `name` *(string, required)*
*   **Tag**
    *   `name` *(string, required)*

### **Relationships**

*   `Article` **belongs to** one `Category`.
*   `Article` **belongs to many** `Tags`.
*   `Tag` **belongs to many** `Articles`.

---

## 🛠️ **Laravel Features Checklist**

Your blog should showcase your understanding of these fundamental Laravel concepts:

### **🛣️ Routing & Controllers**

| Feature | Status |
| :--- | :---: |
| Callback Functions & `Route::view()` | ☐ |
| Routing to Controller Methods | ☐ |
| Route Parameters (e.g., article ID) | ☐ |
| Named Routes | ☐ |
| Route Groups (e.g., for admin) | ☐ |

### **🎨 Blade Templating**

| Feature | Status |
| :--- | :---: |
| Displaying Data (`{{ }}`) | ☐ |
| Control Structures (`@if`, `@else`, `@foreach`) | ☐ |
| Layouts (`@extends`, `@section`, `@yield`) | ☐ |
| Partials (`@include`) | ☐ |
| Blade Components | ☐ |

### **🔐 Authentication**

| Feature | Status |
| :--- | :---: |
| Default `User` Model Usage | ☐ |
| Auth Checks (Controller & Blade) | ☐ |
| `auth` Middleware | ☐ |

### **🗄️ Database Fundamentals**

| Feature | Status |
| :--- | :---: |
| Database Migrations | ☐ |
| Eloquent Models & MVC Flow | ☐ |
| Relationships (`belongsTo`, `hasMany`, `belongsToMany`) | ☐ |
| Eager Loading (Prevent N+1) | ☐ |

### **🔄 Full CRUD Operations**

| Feature | Status |
| :--- | :---: |
| Resource Routes (`Route::resource`) | ☐ |
| Resource Controllers | ☐ |
| Forms & Validation (including Form Requests) | ☐ |
| File Uploads & Storage | ☐ |
| Data Pagination | ☐ |

---

## ✅ **Submission Process**

1.  **Fork** this repository.
2.  **Build** your personal blog application meeting the requirements.
3.  **Commit** your code cleanly.
4.  Create a **Pull Request** with your solution.

---
