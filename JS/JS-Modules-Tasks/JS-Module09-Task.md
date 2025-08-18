# **Module 09 – Web Storage**

````markdown
# 🟦 Module 09: Web Storage (localStorage & sessionStorage)

## 🎯 Task: Notes App with Persistence

Build a notes app where users can write notes, and the app saves them using **Web Storage**.

---

## ✅ Requirements

- Allow users to type a note in a text area and click **Save**.
- Notes are stored in **localStorage** and remain after refresh.
- Store the "last session note" in **sessionStorage**.
- Provide a button to **clear all notes**.

---

## 📌 Skeleton Code

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Notes App</title>
    <style>
      body {
        font-family: Arial;
        margin: 20px;
      }
      textarea {
        width: 100%;
        height: 100px;
      }
      button {
        margin: 5px;
        padding: 8px 12px;
      }
      #notes {
        margin-top: 20px;
      }
    </style>
  </head>
  <body>
    <h1>📝 Notes App</h1>
    <textarea id="noteInput" placeholder="Write your note here..."></textarea
    ><br />
    <button id="saveNote">Save Note</button>
    <button id="clearNotes">Clear All</button>
    <div id="notes"></div>
  </body>
</html>
```
````

---

## 🧠 Learning Outcomes

- Storing and retrieving data from localStorage.
- Using sessionStorage for temporary session data.
- Persisting data across page reloads.
- Rendering stored data dynamically.
