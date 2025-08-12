# 🔐 Module 5: Authentication & Middleware in Laravel

## 🎯 Task: Add User Authentication and Protected Routes

### Objective
Secure your blog by adding user login and restricting post creation to authenticated users.

### ✅ Requirements

1. **Install Laravel Breeze**
   - ```bash
     composer require laravel/breeze --dev
     php artisan breeze:install
     npm install && npm run dev
     php artisan migrate
     ```

2. **Protect Post Creation**
   - Add a `create()` and `store()` method in `PostController`
   - Apply `auth` middleware:
     ```php
     public function __construct()
     {
         $this->middleware('auth')->only(['create', 'store']);
     }
     ```

3. **Add Auth Links to Navbar**
   - In `layouts/app.blade.php`, show:
     - "Login" / "Register" if guest
     - "Dashboard" / "Logout" if logged in
   - Use `@auth` and `@guest` directives

4. **Test Authentication**
   - Register a new user
   - Try to access `/posts/create` as guest → should redirect to login
   - Log in and verify access

5. **Update Seeder (Optional)**
   - Seed a user for testing:
     ```php
     User::factory()->create([
         'name' => 'Admin',
         'email' => 'admin@example.com',
     ]);
     ```

### 📦 Deliverables
- GitHub repo with:
  - Breeze installed
  - Protected routes using middleware
  - Auth-aware navigation
  - `README.md` explaining auth flow

### 💡 Tip
Laravel Middleware acts like a gatekeeper — perfect for permissions, logging, and security.