# 🐘 Module 3: Arrays and Strings

## 🎯 Objectives
By the end of this module, you will:
- Work with strings and use PHP’s built-in string functions.
- Create, manipulate, and access arrays.
- Apply string and array functions in real-world mini-problems.

---

## **Part 1: String Functions**

### 1. String Case Conversion
Write a PHP script to:
- Convert the entered string to uppercase.
- Convert the entered string to lowercase.
- Make the first letter uppercase.
- Make the first letter of each word uppercase.

---

### 2. Split Numeric String into Time
**Sample Input:**  
`'085119'`  
**Expected Output:**  
`08:51:19`

---

### 3. Search for a Word in a Sentence
Check whether the sentence contains a specific word.  
**Sample Sentence:**  
`I am a full stack developer at orange coding academy`  
**Sample Word:**  
`Orange`  
**Expected Output:**  
`Word Found!`

---

### 4. Extract File Name from URL
**Sample Input:**  
`www.orange.com/index.php`  
**Expected Output:**  
`index.php`

---

### 5. Extract Username from Email
**Sample Input:**  
`info@orange.com`  
**Expected Output:**  
`info`

---

### 6. Get Last Three Characters
**Sample Input:**  
`info@orange.com`  
**Expected Output:**  
`com`

---

### 7. Generate a Random Password (Without `rand()`)
Generate passwords from the given string:  
```

1234567890ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz

```
**Expected Output:**  
`254ABCc` or `h242sfeDAFEe32` (random each time)

---

### 8. Replace First Word in a Sentence
Replace the first word of a sentence with another word.  
**Example:**  
Input: `"Our new trainee is so genius."`  
Replace `"Our"` with `"That"`  
Output: `"That new trainee is so genius."`

---

### 9. Find First Difference Between Two Strings
Compare:
```

String 1: dragonball
String 2: dragonboll

```
Expected:  
`First difference at position 7: "a" vs "o"`

---

### 10. Split String into Array
Use `var_dump()` to display the array.
**Example:**  
`"Twinkle, twinkle, little star."`

---

### 11. Next Letter in Alphabet
If input is `'a'` → Output `'b'`  
If input is `'z'` → Output `'a'`

---

### 12. Insert String at Position
Insert `"quick"` into `'The brown fox'` → `'The quick brown fox'`

---

### 13. Remove Leading Zeros
`'0000657022.24'` → `'65722.24'`

---

### 14. Remove Part of a String
Remove `'fox'` from `'The quick brown fox jumps over the lazy dog'`

---

### 15. Remove Trailing Dashes
`'The quick brown fox jumps over the lazy dog---'` →  
`'The quick brown fox jumps over the lazy dog'`

---

### 16. Remove Special Characters
From: `"\1\+2/3*2:2-3/4*3"`  
Output: `'1 2 3 2 2 3 4 3'`

---

### 17. Get First 5 Words
From: `'The quick brown fox jumps over the lazy dog'`  
Output: `'The quick brown fox jumps'`

---

### 18. Remove Commas from Number
`'2,543.12'` → `2543.12`

---

### 19. Print Letters a–z
```

a b c d e f g ... z

```

---

## **Part 2: Arrays**

### 20. Create and Access Indexed Array
1. Create an array of 5 fruits.
2. Print each fruit using a `for` loop.

---

### 21. Associative Array Example
Create an associative array with:
- `"name"` → `"John"`
- `"age"` → `25`
- `"city"` → `"Amman"`
Print: `"My name is John, I am 25, and I live in Amman."`

---

### 22. Multidimensional Array
Store data for 3 students: name, grade, subject.  
Loop and print them in a table.

---

### 23. Sort Arrays
- Sort ascending and descending (`sort()`, `rsort()`).
- Sort associative arrays by value and key (`asort()`, `ksort()`).

---

### 24. Merge Arrays
Merge two arrays:  
`["red", "green"]` and `["blue", "yellow"]`

---

### 25. Remove Duplicate Values
From: `["red", "blue", "red", "green", "blue"]`  
Expected: `["red", "blue", "green"]`

---

### 26. Search for Value in Array
Check if `"apple"` exists in `["banana", "apple", "mango"]`

---

### 27. Array Slicing
From: `["A", "B", "C", "D", "E"]`  
Slice last 3 elements.

---

### 28. Array Push & Pop
Demonstrate `array_push()`, `array_pop()`, `array_shift()`, and `array_unshift()`.

---

### 29. Combine Keys and Values
Keys: `["name", "age", "city"]`  
Values: `["Ali", 30, "Irbid"]`  
Output associative array.

---

### 30. Count Array Elements
Count items in:
`["pen", "pencil", "eraser", "pen"]`

---

💡 **Extra Challenge Ideas**
- Reverse a string without using `strrev()`.
- Convert a sentence into an array of words, then back into a sentence.
- Create a random team picker from an array of names.
- Count how many times each letter appears in a string.
- Find the longest word in a sentence.

---

📌 **Tips for Students:**
- Test your scripts in separate `.php` files.
- Use `var_dump()` to inspect variables.
- Experiment with different inputs to understand function behavior.

