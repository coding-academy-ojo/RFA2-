# 🟦 Module 04: DOM Manipulation

## 🎯 Task: To-Do List App (Basic)

Create a simple To-Do List app where users can add tasks, mark them as complete, and delete them.

---

## ✅ Requirements

- Use DOM methods (`getElementById`, `querySelector`, etc.) to select elements.
- Add new tasks dynamically when the user clicks **Add**.
- Mark tasks as complete with a **line-through** style.
- Delete tasks from the list.
- Apply CSS classes for styling.

---

## 📌 Skeleton Code

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>To-Do App</title>
    <style>
      body {
        font-family: Arial;
        margin: 20px;
      }
      ul {
        list-style: none;
        padding: 0;
      }
      li {
        padding: 8px;
        border: 1px solid #ccc;
        margin-bottom: 5px;
      }
      .completed {
        text-decoration: line-through;
        color: gray;
      }
    </style>
  </head>
  <body>
    <h1>To-Do App</h1>
    <input type="text" id="taskInput" placeholder="New Task" />
    <button id="addTask">Add</button>
    <ul id="taskList"></ul>
  </body>
</html>
```

```

---

## 🧠 Learning Outcomes

- DOM selection & manipulation.
- Event handling (click, input).
- Adding and removing elements dynamically.
```
