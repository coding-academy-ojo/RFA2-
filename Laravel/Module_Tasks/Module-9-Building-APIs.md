# 🔗 Module 9: Building APIs in Laravel

## 🎯 Task: Expose Task Data via a RESTful JSON API

### Objective
Create a secure API endpoint to retrieve tasks in JSON format, preparing for future frontend integration (e.g., React, mobile apps).

### ✅ Requirements

1. **Create API Routes**
   - In `routes/api.php`:
     ```php
     Route::apiResource('tasks', TaskApiController::class)->middleware('auth:sanctum');
     ```

2. **Install Laravel Sanctum**
   - ```bash
     composer require laravel/sanctum
     php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"
     php artisan migrate
     ```

3. **Generate API Controller**
   - ```bash
     php artisan make:controller TaskApiController --api
     ```
   - Implement `index()`, `show()`, `store()`, etc.

4. **Return JSON Responses**
   - In `index()`:
     ```php
     return response()->json(auth()->user()->tasks);
     ```
   - Use API Resources (optional bonus):
     ```bash
     php artisan make:resource TaskResource
     ```

5. **Test the API**
   - Use Postman or browser with token:
     - Register a user
     - Generate token in database or via login API
     - Call `GET /api/tasks` with header: `Authorization: Bearer {token}`

6. **Secure the API**
   - Apply `auth:sanctum` middleware
   - Ensure users only access their own tasks

### 📦 Deliverables
- GitHub repo with:
  - API routes and controller
  - Sanctum authentication
  - JSON responses
  - `README.md` with API documentation (endpoints, auth method)

### 💡 Tip
APIs power modern apps — this skill opens doors to full-stack, mobile, and backend roles.