# Task 4: PHP OOP Concepts – Classes, Inheritance, Encapsulation & Abstraction

## Modules Covered

* Module 4: PHP OOP Basics
* Module 5: Inheritance in PHP OOP
* Module 6: Polymorphism in PHP OOP
* Module 7: Interfaces and Implementations in PHP OOP
* Module 8: Abstract Classes and Methods in PHP OOP

---

## 🎯 Goal

Learn and practice **core Object-Oriented Programming (OOP) concepts in PHP**:

* Creating classes and objects
* Implementing inheritance and polymorphism
* Applying encapsulation with access modifiers
* Using abstraction with abstract classes and methods

---

## Steps

### ** 1: Class and Object Creation**

* Create a `Car` class with properties:

  * `make`
  * `model`
  * `year`
* Define methods:

  * Setters (`setMake()`, `setModel()`, `setYear()`)
  * Getters (`getMake()`, `getModel()`, `getYear()`)
* Instantiate at least **3 Car objects** and print their details.

---

### ** 2: Inheritance and Polymorphism**

* Create a `Vehicle` base class with property:

  * `type`
* Define method:

  * `move()` → Prints a generic movement message.
* Create derived classes:

  * `Car` (inherits from `Vehicle`)
  * `Bike` (inherits from `Vehicle`)
* Override the `move()` method in each derived class:

  * Car → “The car drives on the road.”
  * Bike → “The bike rides on two wheels.”
* Demonstrate **polymorphism** by calling `move()` on different objects.

---

### ** 3: Encapsulation**

* Modify the `Car` class:

  * Make its properties **private** (`make`, `model`, `year`).
  * Add **getter** and **setter** methods for each property.
* Demonstrate:

  * Direct property access (should fail).
  * Access via getter/setter (works correctly).

---

### ** 4: Abstraction**

* Create an **abstract class** `Shape` with abstract method:

  * `calculateArea()`
* Create two concrete classes:

  * `Circle` → implements `calculateArea()` using radius.
  * `Rectangle` → implements `calculateArea()` using width × height.
* Instantiate both classes and call `calculateArea()`.

---

## 📦 Deliverables

* `task1_car_class.php` → Car class with objects
* `task2_inheritance.php` → Vehicle, Car, Bike with polymorphism
* `task3_encapsulation.php` → Car class with private properties and setters/getters
* `task4_abstraction.php` → Shape, Circle, Rectangle with area calculation
* README file summarizing:

  * Concepts learned in each task
  * How to run each PHP file

---

## 💡 Extra Tips

* Always start class names with **uppercase letters** (e.g., `Car`, `Vehicle`).
* Use **private** for encapsulation and expose data through getters/setters.
* **Polymorphism** means one method behaves differently depending on the object.
* **Abstract classes** cannot be instantiated; they must be extended by concrete classes.
* Run each file in the browser (`http://localhost/...`) or CLI (`php taskX.php`) to test.
