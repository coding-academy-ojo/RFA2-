# 🐘 Module 5: Functions in PHP

## 🎯 Objectives

By the end of this module, you will be able to:

* Understand the syntax and structure of PHP functions.
* Create **user-defined functions** with and without parameters.
* Use **return values** effectively to pass results back from functions.
* Implement **logic-based functions** for tasks like checking primes, palindromes, and Armstrong numbers.
* Manipulate **strings** and **arrays** using functions.
* Apply **recursive functions** for problems like factorials and Fibonacci.
* Use PHP’s built-in functions for string and array handling.
* Write reusable, modular code that improves readability and reduces repetition.

---

## 1. Check if a Number is Prime
**Description:**  
Write a PHP function to check if the inserted number is a prime number.

**Sample Input:**
```

3

```
**Expected Output:**
```

3 is a prime number

```

---

## 2. Reverse a String
**Description:**  
Write a PHP function to reverse a given string.

**Sample Input:**
```

remove

```
**Expected Output:**
```

evomer

```

---

## 3. Check if String is All Lowercase
**Description:**  
Write a PHP function to check if all characters in a string are lowercase.

**Sample Input:**
```

remove

```
**Expected Output:**
```

Your String is Ok

```

---

## 4. Swap Two Variables
**Description:**  
Write a PHP function to swap the values of two variables.

**Sample Input:**
```

x = 12, y = 10

```
**Expected Output:**
```

y = 12, x = 10

```

---

## 5. Armstrong Number Check
**Description:**  
Write a PHP function to check if a number is an Armstrong number.  
*(An Armstrong number is one where the sum of the cubes of its digits equals the number itself.)*

**Sample Input:**
```

407

```
**Expected Output:**
```

407 is Armstrong Number

```

---

## 6. Palindrome String Check
**Description:**  
Write a PHP function that checks whether a passed string is a palindrome.

**Sample Input:**
```

Eva, can I see bees in a cave?

```
**Expected Output:**
```

Yes it is a palindrome

```

---

## 7. Remove Duplicate Elements from an Array
**Description:**  
Write a PHP function to remove duplicate elements from an array.

**Sample Input:**
```

array(2, 4, 7, 4, 8, 4)

```
**Expected Output:**
```

2, 4, 7, 8

```

---

## 8. Factorial of a Number *(Extra Task)*
**Description:**  
Write a recursive PHP function to calculate the factorial of a number.

**Sample Input:**
```

5

```
**Expected Output:**
```

120

```

---

## 9. Count the Number of Words in a String *(Extra Task)*
**Description:**  
Write a PHP function that counts the number of words in a string.

**Sample Input:**
```

"PHP is awesome"

```
**Expected Output:**
```

3

```

---

## 10. Generate Fibonacci Sequence *(Extra Task)*
**Description:**  
Write a PHP function to generate the first N numbers in the Fibonacci sequence.

**Sample Input:**
```

N = 8

```
**Expected Output:**
```

0, 1, 1, 2, 3, 5, 8, 13

```
---

### 📦 Deliverables

* `index.php` with:

  * Simple PHP output
  * PHP embedded inside HTML
  * At least one PHP variable and function call
* A screenshot of the page in the browser.
---

### **💡 Extra Tips**

💡 **Naming Matters** – Use descriptive function names (e.g., `isPrimeNumber()` instead of `check()`) so your code is easier to read later.

💡 **One Function, One Purpose** – Keep functions focused. A function should only do one logical task.

💡 **Return Values vs. Echo** – If you want to use the result elsewhere, `return` it instead of printing with `echo`.

💡 **Test with Edge Cases** – When writing functions like palindrome checks, test with:

* Empty strings
* Uppercase/lowercase combinations
* Strings with spaces and punctuation

💡 **Recursion vs. Loops** – Some problems (factorial, Fibonacci) can be solved with loops or recursion. Try both to understand the difference.

💡 **Avoid Duplicates** – If you have two functions doing the same thing (like your duplicate swap task), combine them into one and reuse it.

💡 **Use Built-in Functions** – PHP has many built-in helpers (`strrev()`, `array_unique()`, `ctype_lower()`). Learn them to save time.

💡 **Comment Your Code** – Write short notes above functions explaining:

```php
// Checks if a number is prime by testing divisibility
function isPrime($n) { ... }
```

---
