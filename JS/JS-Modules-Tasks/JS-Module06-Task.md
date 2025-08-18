# **Module 06 – JSON**

````markdown
# 🟦 Module 06: JSON

## 🎯 Task: Student Records Parser (Console App)

Work with JSON data to store and display student information.

---

## ✅ Requirements

- Create a JSON string with an array of student objects (`name`, `age`, `grade`).
- Parse the JSON string into JavaScript objects.
- Loop through and display all students.
- Convert updated records back into a JSON string.

---

## 📌 Example Behavior

```js
const studentsJSON =
  '[{"name":"Ali","age":20,"grade":"A"},{"name":"Sara","age":22,"grade":"B"}]';

let students = JSON.parse(studentsJSON);

students.forEach((s) => console.log(`${s.name} - ${s.grade}`));

students.push({ name: "Omar", age: 21, grade: "C" });

console.log(JSON.stringify(students));
```
````

---

🧠 Learning Outcomes

- Understanding JSON structure.
- Converting between JSON and JavaScript objects.
- Iterating over parsed data.
- Preparing data for storage or API communication.
