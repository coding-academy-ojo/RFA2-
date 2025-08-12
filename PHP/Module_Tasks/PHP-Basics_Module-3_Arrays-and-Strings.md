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
## **Part 3: Arrays Advance**

## 1. Generate a Paragraph Using Array Values
**Task:**  
Write a script to generate the following paragraph:

> "The memory of that scene for me is like a frame of film forever frozen at that moment: the red carpet, the green lawn, the white house, the leaden sky. The new president and his first lady. – Richard M. Nixon"

The words **red**, **green**, and **white** should come from the `$colors` array.

---

## 2. Display Colors as Unordered List
```php
$colors = array('white', 'green', 'red');
````

**Expected Output:**

* green
* red
* white

---

## 3. Display Capitals and Countries Sorted by Capital Name

```php
$cities = array(
    "Italy" => "Rome", "Luxembourg" => "Luxembourg", "Belgium" => "Brussels",
    "Denmark" => "Copenhagen", "Finland" => "Helsinki", "France" => "Paris",
    "Slovakia" => "Bratislava", "Slovenia" => "Ljubljana", "Germany" => "Berlin",
    "Greece" => "Athens", "Ireland" => "Dublin", "Netherlands" => "Amsterdam",
    "Portugal" => "Lisbon", "Spain" => "Madrid"
);
```

**Expected Output:**

```
The capital of Netherlands is Amsterdam
The capital of Greece is Athens
The capital of Germany is Berlin
...
```

---

## 4. Display the First Element of an Array

```php
$color = array(4 => 'white', 6 => 'green', 11 => 'red');
```

**Expected Output:**

```
white
```

---

## 5. Insert a Specific Item in an Array

**Sample Input:**

```
Array: 1 2 3 4 5  
Location: 4  
New Item: $
```

**Expected Output:**

```
1 2 3 $ 4 5
```

---

## 6. Sort Associative Array by Key (Ascending)

```php
$fruits = array("d" => "lemon", "a" => "orange", "b" => "banana", "c" => "apple");
```

**Expected Output:**

```
c = apple
b = banana
d = lemon
a = orange
```

---

## 7. Average Temperature & Extremes

**Sample Input:**

```
78, 60, 62, 68, 71, 68, 73, 85, 66, 64, 76, 63, 75, 76, 73, 68, 
62, 73, 72, 65, 74, 62, 62, 65, 64, 68, 73, 75, 79, 73
```

**Expected Output:**

```
Average Temperature is: 70.6
List of seven lowest temperatures: 60, 62, 63, 63, 64, ...
List of seven highest temperatures: 76, 78, 79, 81, 85, ...
```

---

## 8. Merge Two Arrays

```php
$array1 = array("color" => "red", 2, 4);
$array2 = array("a", "b", "color" => "green", "shape" => "trapezoid", 4);
```

**Expected Output:**

```
Array
(
    [color] => green
    [0] => 2
    [1] => 4
    [2] => a
    [3] => b
    [shape] => trapezoid
    [4] => 4
)
```

---

## 9. Convert Array Strings to Uppercase

```php
$colors = array("red","blue","white","yellow");
```

**Expected Output:**

```
RED
BLUE
WHITE
YELLOW
```

---

## 10. Convert Array Strings to Lowercase

```php
$colors = array("RED","BLUE","WHITE","YELLOW");
```

**Expected Output:**

```
red
blue
white
yellow
```

---

## 11. Numbers Between 200 and 250 Divisible by 4

**Expected Output:**

```
200, 204, 208, 212, 216, 220, 224, 228, 232, 236, 240, 244, 248
```

---

## 12. Shortest & Longest String Length in Array

```php
$words = array("abcd","abc","de","hjjj","g","wer");
```

**Expected Output:**

```
The shortest array length is 1. The longest array length is 4.
```

---

## 13. Generate 10 Unique Random Numbers in a Range

**Sample Input:**

```
Range: 11 to 20
```

**Sample Output:**

```
17 16 13 20 14 19 18 15 11 12
```

---

## 14. Lowest Non-Zero Integer

```php
$array1 = array(2, 0, 10, 12, 6);
```

**Expected Output:**

```
2
```

---

## 15. Sort Array of Positive Integers (Any Algorithm)

**Sample Input:**

```
Array: 5, 3, 1, 3, 8, 7, 4, 1, 1, 3
```

**Expected Result:**

```
8, 7, 5, 4, 3, 3, 3, 1, 1, 1
```

---

## 16. Floor Decimal Numbers with Precision

**Sample Data:**

```
1.155, 2, "."
100.25781, 4, "."
-2.9636, 3, "."
```

**Expected Output:**

```
1.15
100.2578
-2.964
```

---

## 17. Merge Two Comma-Separated Lists (Unique Values)

**Sample Input:**

```
list1 = "4, 5, 6, 7"
list2 = "4, 5, 7, 8"
```

**Sample Output:**

```
4, 5, 6, 7, 8
```

---

## 18. Remove Duplicate Entries from Array

**Sample Input:**

```
4, 5, 6, 7, 4, 7, 8
```

**Sample Output:**

```
4, 5, 6, 7, 8
```

---

## 19. Check if Array is Subset of Another

**Sample Input:**

```
array1 = 'a','1','2','3','4'
array2 = 'a','3'
```

**Sample Output:**

```
array2 is a subset array from array1
```
---

### 📦 Deliverables

* `index.php` with:

  * Simple PHP output
  * PHP embedded inside HTML
  * At least one PHP variable and function call
* A screenshot of the page in the browser.

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

