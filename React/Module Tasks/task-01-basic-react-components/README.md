# Task 1: Basic React Setup & Component Architecture

## Modules Covered
1, 2, 3

## 🎯 Goal
Set up a React project using Vite and build static components to display a list of books.

---

## Steps

1. **Create a GitHub repository** named `Library-App`.

2. **Initialize React app using Vite:**
   ```bash
   npm create vite@latest
   # Choose React (JavaScript)
   cd Library-App
   npm install

Absolutely! Here are the **5 task files** fully written out in Markdown, ready for GitHub or your LMS.

---

## task-01-basic-react-components.md

````markdown
# Task 1: Basic React Setup & Component Architecture

## Modules Covered
1, 2, 3

## 🎯 Goal
Set up a React project using Vite and build static components to display a list of books.

---

## Steps

1. **Create a GitHub repository** named `Library-App`.

2. **Initialize React app using Vite:**
   ```bash
   npm create vite@latest
   # Choose React (JavaScript)
   cd Library-App
   npm install
````

3. **Push initial app to GitHub:**

   ```bash
   git init
   git add .
   git commit -m "Initial Vite setup for Library App"
   git branch -M main
   git remote add origin <your-repo-url>
   git push -u origin main
   ```

4. **Create initial state object with at least 4 books** (including the 2 sample books):

   ```javascript
   export const initState = {
     books: [
       { id: 1, title: "مقدمة ابن خلدون", author: "ابن خلدون", isbn: "1289499030" },
       { id: 2, title: "الحاوي في الطب", author: "ابو بكر الرازي", isbn: "893847239479" },
       { id: 3, title: "البخلاء", author: "الجاحظ", isbn: "1928304823" },
       { id: 4, title: "ألف ليلة وليلة", author: "مجهول", isbn: "8472938472" }
     ]
   };
   ```

5. **Build the component structure:**

   * `Header`
   * `Main` (reads books from state and displays them)
   * `Footer`
   * `BookCard` (displays each book’s details)

6. **Display the books as cards in `Main` component**, passing the book data as props to `BookCard`.

---

## Submission

* Push your code to GitHub with commit message:

  ```
  feat: add initial static components and book list
  ```

````

---


