## task-02-state-management-hooks.md

```markdown
# Task 2: State Management & React Hooks

## Modules Covered
4, 5

## 🎯 Goal
Convert the static book data into dynamic state using React hooks.

---

## Steps

1. **Replace static book data with React's `useState` hook** inside your components (likely in `Main`).

2. **Manage books state dynamically**:
   - Initialize state with the `initState.books`.
   - Prepare for future operations like adding, editing, or deleting books.

3. **Ensure books data flows properly through props** to child components like `BookCard`.

Example:
```jsx
import { useState } from 'react';
import { initState } from '../data';

function Main() {
  const [books, setBooks] = useState(initState.books);

  return (
    <div>
      {books.map(book => (
        <BookCard key={book.id} {...book} />
      ))}
    </div>
  );
}
````

---

## Submission

* Push your code with commit message:

  ```
  feat: convert static book data to useState hook
  ```

````

---
