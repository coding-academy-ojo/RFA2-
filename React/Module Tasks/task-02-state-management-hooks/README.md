Alright 👍
Here’s the **Module 2** `.md` file for the **Library Management App – Part 1** task, GitHub-ready.

---

```markdown
# 📚 Module 2 – Library Management App (Part 1)

## 🎯 Goal
Set up the **Library Management App** project using React with Vite, create the initial state, and display books using components.

---

## 📋 Steps

### 1️⃣ Create a GitHub Repository
- Name it:
```

Library-App

````

### 2️⃣ Initialize React App (using Vite)
```bash
npm create vite@latest
# Select React (JavaScript)
cd Library-App
npm install
````

### 3️⃣ Push Initial App to GitHub

```bash
git init
git add .
git commit -m "Initial Vite setup for Library App"
git branch -M main
git remote add origin <your-repo-url>
git push -u origin main
```

### 4️⃣ Create Initial State

Inside your `src` folder, create `data.js` and add:

```javascript
export const initState = {
  books: [
    {
      id: 1,
      title: "مقدمة ابن خلدون",
      author: "ابن خلدون",
      isbn: "1289499030"
    },
    {
      id: 2,
      title: "الحاوي في الطب",
      author: "ابو بكر الرازي",
      isbn: "893847239479"
    },
    {
      id: 3,
      title: "البخلاء",
      author: "الجاحظ",
      isbn: "1928304823"
    },
    {
      id: 4,
      title: "ألف ليلة وليلة",
      author: "مجهول",
      isbn: "8472938472"
    }
  ]
};
```

> 💡 You must add **at least 2 extra books**.

---

### 5️⃣ Create Component Structure

* `Home` (main page)

  * `Header`
  * `Main`
  * `Footer`
* `BookCard` (for displaying each book)

📂 **Suggested Folder Structure:**

```
src/
 ├── components/
 │    ├── Header.jsx
 │    ├── Main.jsx
 │    ├── Footer.jsx
 │    ├── BookCard.jsx
 ├── pages/
 │    ├── Home.jsx
 ├── data.js
 ├── App.jsx
 ├── main.jsx
```

---

### 6️⃣ Display Books in Cards

* Pass `books` from `initState` into `Main` component.
* In `Main`, map over `books` and render `BookCard` for each book.

Example `BookCard`:

```jsx
function BookCard({ title, author, isbn }) {
  return (
    <div className="book-card">
      <h3>{title}</h3>
      <p>By: {author}</p>
      <small>ISBN: {isbn}</small>
    </div>
  );
}

export default BookCard;
```

---

## ✅ Submission

Push your code to GitHub with the commit message:

feat: add initial state and basic components for Library App

