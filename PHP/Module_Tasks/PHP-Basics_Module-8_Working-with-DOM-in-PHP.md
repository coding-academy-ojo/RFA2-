# 🐘 Module 8: Working with DOM in PHP

## 🎯 Objectives

Use PHP DOM manipulation and an array of products (provided in `index.php`) to display a collection of mobile phones in card format using **Boosted** (Orange's Bootstrap-based framework).

<img width="1920" height="3701" alt="screencapture-eshop-orange-jo-en-devices-accessories-mobile-phone-2025-08-13-12_07_23" src="https://github.com/user-attachments/assets/1dc0abb2-37d9-4df3-8ad7-cf344418fcfc" />

---
## 🎯 Task: Display Cards using PHP

## 📄 Scenario

Orange Jordan’s e-shop needs a simple mobile phone listing page.
You have an **array of phones** in `index.php` (already provided).
Your task is to generate a **responsive card layout** where each phone’s image, name, and price are displayed beautifully.

---

## ✅ Requirements

1. **Setup Project**

   * Download the starter code from this repository.
   * create `index.php` — you’ll find an array containing phone details (name, price, image link).
     
index.php content:
```
<?php 
$phones = [
    [ 
     'name' => 'Samsung Galaxy Note 20 Ultra',
     'img_url' =>'https://eshop.orange.jo/app-images/thumbs/0001115_samsung-galaxy-note-20-ultra_220.png',
    'rate' => '5',
    'brand' => 'Samsung',
    'price' => 'JOD 759.00',
    'is_out_of_stock' => '1'
    ],
    [ 
     'name' => 'INFINIX Zero 8',
     'img_url' =>'https://eshop.orange.jo/app-images/thumbs/0001278_infinix-zero-8_220.jpeg',
    'rate' => '0',
    'brand' => 'Infinix',
    'price' => 'JOD 205.00',
    'is_out_of_stock' => '1'
    ],
    [ 
     'name' => 'Apple iPhone 12 Pro',
     'img_url' =>'https://eshop.orange.jo/app-images/thumbs/0001495_apple-iphone-12-pro_220.jpeg',
    'rate' => '0',
    'brand' => 'Apple',
    'price' => 'JOD 973.00',
    'is_out_of_stock' => '1'

    ],
    [ 
     'name' => 'ITEL A48',
     'img_url' =>'https://eshop.orange.jo/app-images/thumbs/0001495_apple-iphone-12-pro_220.jpeg',
    'rate' => '0',
    'brand' => 'iTel',
    'price' => 'JOD 66.00'
    ],
    [ 
     'name' => 'Samsung Galaxy S21 Ultra',
     'img_url' =>'https://eshop.orange.jo/app-images/thumbs/0001485_samsung-galaxy-s21-ultra_220.jpeg',

    'rate' => '0',
    'brand' => 'Samsung',
    'price' => 'JOD 799.00'
    ],
    
    [ 
     'name' => 'Galaxy A52',
     'img_url' =>'https://eshop.orange.jo/app-images/thumbs/0002097_galaxy-a52_220.jpeg',
    'rate' => '0',
    'brand' => 'Samsung',
    'price' => 'JOD 267.00'
    ],
];

?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mobile Phone | Orange Jordan E shop</title>
    <!-- Copyright © 2014 Monotype Imaging Inc. All rights reserved -->
<link href="https://cdn.jsdelivr.net/npm/boosted@5.1.3/dist/css/orange-helvetica.min.css" rel="stylesheet" integrity="sha384-ARRzqgHDBP0PQzxQoJtvyNn7Q8QQYr0XT+RXUFEPkQqkTB6gi43ZiL035dKWdkZe" crossorigin="anonymous">
<link href="https://cdn.jsdelivr.net/npm/boosted@5.1.3/dist/css/boosted.min.css" rel="stylesheet" integrity="sha384-Di/KMIVcO9Z2MJO3EsrZebWTNrgJTrzEDwAplhM5XnCFQ1aDhRNWrp6CWvVcn00c" crossorigin="anonymous">
</head>
<body>
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">
      <img src="https://boosted.orange.com/docs/5.1/assets/brand/orange-logo.svg" width="50" height="50" role="img" alt="Boosted" loading="lazy">
    </a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Link</a>
        </li>
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            Dropdown
          </a>
          <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
            <li><a class="dropdown-item" href="#">Action</a></li>
            <li><a class="dropdown-item" href="#">Another action</a></li>
            <li><hr class="dropdown-divider"></li>
            <li><a class="dropdown-item" href="#">Something else here</a></li>
          </ul>
        </li>
        <li class="nav-item">
          <a class="nav-link disabled">Disabled</a>
        </li>
      </ul>
      <form class="d-flex">
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
        <button class="btn btn-primary" type="submit">Search</button>
      </form>
    </div>
  </div>
</nav>
<script src="https://cdn.jsdelivr.net/npm/boosted@5.1.3/dist/js/boosted.bundle.min.js" integrity="sha384-5thbp4uNEqKgkl5m+rMBhqR+ZCs+3iAaLIghPWAgOv0VKvzGlYKR408MMbmCjmZF" crossorigin="anonymous"></script>
</body>
</html>

```

2. **Integrate Boosted CSS**

   * Use Boosted's CDN from the documentation:
     [https://boosted.orange.com/docs/5.1/getting-started/introduction/](https://boosted.orange.com/docs/5.1/getting-started/introduction/)
   * Include necessary CSS/JS in your HTML `<head>`.

3. **Loop Through Array in PHP**

   * Use `foreach` to iterate through the `$phones` array.
   * For each phone:

     * Display its **image**.
     * Display its **name**.
     * Display its **price**.

4. **Use Card Layout**

   * Use Boosted’s **card component**.
   * Each phone should be in its own card.
   * Cards should be responsive (adjust to screen size).

5. **Optional Styling**

   * Add hover effects.
   * Add “Buy Now” buttons (no functionality needed).

---

## 💡 Tips

* Look at **Boosted's card examples**: [https://boosted.orange.com/docs/5.1/components/card/](https://boosted.orange.com/docs/5.1/components/card/)
* Make sure images have the same height for a clean layout.
* Use **Bootstrap/Boosted grid system** for alignment.
* Keep the PHP loop clean and modular.

---

## 📦 Deliverables

* **`index.php`** with:

  * Boosted CSS/JS linked.
  * PHP loop generating the phone cards.
* Screenshot of the page with at least **4 phone cards** displayed.
* README.md explaining:

  * How to run the project.
  * Technologies used.
  * Screenshots.

---

## 🚀 Extra Challenge using PHP
1. Add a **search bar** to filter phones by name.
2. Display the number of phones currently shown.
3. Add a **sort dropdown** (Price Low → High, High → Low).
Do you want me to prepare that version next?
