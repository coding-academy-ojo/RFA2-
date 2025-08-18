# 🟦 Module 05: JavaScript ES5

## 🎯 Task: Library System (Console App)

Create a small library system that manages books using **ES5 features** (constructor functions, prototypes).

---

## ✅ Requirements

- Define a `Book` constructor with properties: `title`, `author`, `year`.
- Add a method using **prototype** to display book info.
- Create a `Library` constructor that stores books in an array.
- Add prototype methods to:
  - Add a book.
  - Find a book by title.
  - List all books.

---

## 📌 Example Behavior

```js
let book1 = new Book("The Alchemist", "Paulo Coelho", 1988);
library.addBook(book1);

library.findBook("The Alchemist");
// Output: The Alchemist by Paulo Coelho (1988)

library.listBooks();
// Lists all books added
```

---

## 🧠 Learning Outcomes

- Understanding constructor functions.
- Using prototype inheritance in ES5.
- Managing collections with objects and arrays
