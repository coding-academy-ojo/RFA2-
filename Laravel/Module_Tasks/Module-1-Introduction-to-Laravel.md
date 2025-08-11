# 📦 Module 1: Introduction to Laravel

## 🎯 Task: Set Up Your First Laravel Project & Explore the Basics

### Objective
Get familiar with Laravel by installing it, exploring its folder structure, and customizing the welcome page.

### ✅ Requirements

1. **Install Laravel**
   - Use Composer to create a new Laravel project:
     ```bash
     composer create-project laravel/laravel module1-task
     ```

2. **Start the Development Server**
   - Navigate into the project and start the server:
     ```bash
     cd module1-task
     php artisan serve
     ```
   - Confirm the app runs at `http://127.0.0.1:8000`

3. **Customize the Welcome Page**
   - Open `resources/views/welcome.blade.php`
   - Replace the default content with:
     - A header: `Welcome to Module 1 – Introduction to Laravel`
     - Your name and student ID
     - A short paragraph: "This is my first Laravel app. I’m excited to learn full-stack development!"

4. **Add a Custom Route**
   - In `routes/web.php`, add a new route:
     ```php
     Route::get('/about', function () {
         return '<h1>About Me</h1><p>Hi, I’m [Your Name], a web developer in training.</p>';
     });
     ```
   - Visit `http://127.0.0.1:8000/about` to test.

5. **Document Your Work**
   - Create a `README.md` in your project folder with:
     - Project title
     - Setup instructions
     - Screenshot of both pages (welcome and `/about`)

### 📦 Deliverables
- GitHub repo link containing:
  - Laravel project (exclude `vendor/`, `node_modules/`)
  - `.gitignore`
  - `README.md` with instructions and screenshots

### 💡 Tip
Use `php artisan list` to explore available Artisan commands — Laravel’s powerful CLI tool.