# 🟦 Module 08: Working with APIs

## 🎯 Task: Random Joke Generator

Build a webpage that fetches random jokes from a public API and displays them.

---

## ✅ Requirements

- Use **fetch API** to get a random joke (e.g., from https://official-joke-api.appspot.com/jokes/random).
- Display the joke on the page.
- Add a **button** to fetch a new joke on demand.
- Handle errors gracefully.

---

## 📌 Skeleton Code

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Joke Generator</title>
    <style>
      body {
        font-family: Arial;
        text-align: center;
        margin: 30px;
      }
      #joke {
        font-size: 1.2em;
        margin: 20px 0;
      }
      button {
        padding: 10px 15px;
      }
    </style>
  </head>
  <body>
    <h1>😂 Random Joke Generator</h1>
    <p id="joke">Click the button to load a joke!</p>
    <button id="getJoke">Get Joke</button>
  </body>
</html>
```

---

## 🧠 Learning Outcomes

- Using the fetch API.
- Handling promises with .then() / .catch().
- Updating the DOM with API data.
- Error handling for failed requests.
