# 🐘 PHP Basics – Module 2: PHP Basics

## 🎯 Learning Goals

By the end of these exercises, you will:

* Understand variables, constants, and data types.
* Use operators for calculations and logic.
* Write comments.
* Output text with `echo` and `print`.

---

## 📝 **Exercise 1: Hello PHP Variables**

1. Create a file `variables.php`.
2. Create variables for:

   * Your name
   * Your age
   * Your favorite color
3. Output them like this:

   ```
   My name is Reem, I am 25 years old, and my favorite color is Blue.
   ```
4. Change the variables and run again.

---

## 📝 **Exercise 2: Concatenation Practice**

1. Create `concat.php`.
2. Store first name and last name in separate variables.
3. Use **string concatenation** (`.`) to output your full name:

   ```php
   $fullName = $firstName . " " . $lastName;
   ```
4. Echo:

   ```
   Hello, John Doe!
   ```

---

## 📝 **Exercise 3: Constants**

1. Create `constants.php`.
2. Define a constant for `SITE_NAME` using:

   ```php
   define("SITE_NAME", "PHP Academy");
   ```
3. Output:

   ```
   Welcome to PHP Academy
   ```
4. Try changing the constant value and see what happens if you redefine it.

---

## 📝 **Exercise 4: Arithmetic Operators**

1. Create `math.php`.
2. Create two variables: `$a = 15`, `$b = 4`.
3. Use operators to output:

   * Addition (`+`)
   * Subtraction (`-`)
   * Multiplication (`*`)
   * Division (`/`)
   * Modulus (`%`)
4. Example:

   ```
   15 + 4 = 19
   15 - 4 = 11
   ...
   ```

---

## 📝 **Exercise 5: Assignment Operators**

1. Create `assignment.php`.
2. Start with `$num = 10`.
3. Use:

   ```php
   $num += 5;
   $num -= 3;
   $num *= 2;
   $num /= 4;
   ```
4. Echo each result after the operation.

---

## 📝 **Exercise 6: Comparison Operators**

1. Create `comparison.php`.
2. Compare two numbers using:

   * `==`
   * `===`
   * `!=`
   * `>`
   * `<`
3. Use `var_dump()` to see `true` or `false` outputs.

---

## 📝 **Exercise 7: Increment & Decrement**

1. Create `increment.php`.
2. Start with `$count = 5`.
3. Use:

   ```php
   echo ++$count; // Pre-increment
   echo $count++; // Post-increment
   echo --$count; // Pre-decrement
   echo $count--; // Post-decrement
   ```

---

## 📝 **Exercise 8: Logical Operators**

1. Create `logic.php`.
2. Set:

   ```php
   $age = 20;
   $isStudent = true;
   ```
3. Use:

   * `&&` (AND)
   * `||` (OR)
   * `!` (NOT)
4. Example:

   ```
   Is student and age > 18? true
   ```

---

## 📝 **Exercise 9: Data Types Check**

1. Create `types.php`.
2. Make variables:

   ```php
   $name = "Sara"; // String
   $age = 22;      // Integer
   $price = 19.99; // Float
   $isAdmin = false; // Boolean
   ```
3. Use `var_dump()` and `gettype()` to display type info.

---

## 📝 **Exercise 10: Type Casting**

1. Create `casting.php`.
2. Cast a float to an integer:

   ```php
   $num = 5.99;
   $intNum = (int)$num;
   ```
3. Echo both values.

---

## 📝 **Exercise 11: Swapping Variables**

1. Create `swap.php`.
2. Store `$x = 5`, `$y = 10`.
3. Swap them **without** creating a third variable.

---

## 📝 **Exercise 12: Small Calculator**

1. Create `calculator.php`.
2. Define `$num1` and `$num2`.
3. Output the results of all basic arithmetic operations.

---

## 📝 **Exercise 13: Temperature Converter**

1. Create `temperature.php`.
2. Convert Celsius to Fahrenheit:

   ```
   $celsius = 30;
   $fahrenheit = ($celsius * 9/5) + 32;
   ```
3. Echo the result.

---

## 📝 **Exercise 14: String Functions Practice**

1. Create `string_functions.php`.
2. Use:

   * `strlen()` (length)
   * `strtoupper()` (uppercase)
   * `strtolower()` (lowercase)
   * `str_replace()` (replace)
3. Test on any sentence.

---

## 📝 **Exercise 15: PHP Info**

1. Create `info.php`.
2. Use:

   ```php
   phpinfo();
   ```
3. Run it to see PHP configuration.

---

💡 **Extra Challenge Tasks**

* Create a script that takes two numbers and tells which one is bigger.
* Make a script that calculates the area of a rectangle.
* Reverse a string without using `strrev()`.

