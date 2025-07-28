## Module 12: Building APIs for React Frontend

- 12.1 Introduction to REST APIs
- 12.2 Setting Up API Routes in Laravel (`routes/api.php`)
- 12.3 Creating API Controllers
- 12.4 Sending JSON Responses
- 12.5 Resource Classes (`Http\Resources`)
- 12.6 CORS & API Authentication (Sanctum)
- 12.7 Connecting Laravel API to React (using Axios)
- 12.8 Building a React CRUD Interface

```

### ✅ Suggested Flow for Teaching

---

### 🔹 12.1 Introduction to REST APIs
- What is an API?
- Differences between Web vs API routes
- RESTful structure: GET, POST, PUT, DELETE

---

### 🔹 12.2 Setting Up API Routes
```php
// routes/api.php
Route::get('/users', [UserController::class, 'index']);
Route::post('/users', [UserController::class, 'store']);
Route::put('/users/{id}', [UserController::class, 'update']);
Route::delete('/users/{id}', [UserController::class, 'destroy']);
```

---

### 🔹 12.3 Creating API Controllers
```bash
php artisan make:controller API/UserController
```

---

### 🔹 12.4 Sending JSON Responses
```php
return response()->json(['message' => 'Success', 'data' => $users]);
```

---

### 🔹 12.5 Resource Classes
```bash
php artisan make:resource UserResource
```

```php
// app/Http/Resources/UserResource.php
public function toArray($request)
{
    return [
        'id' => $this->id,
        'name' => $this->name,
        'email' => $this->email,
    ];
}
```

---

### 🔹 12.6 CORS & Authentication
- Enable CORS in `config/cors.php`
- Install Sanctum for token-based auth:
```bash
composer require laravel/sanctum
php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"
php artisan migrate
```

---

### 🔹 12.7 Connecting React to Laravel API
- Install Axios in React:
```bash
npm install axios
```

- Fetch data example:
```js
axios.get('http://localhost:8000/api/users')
  .then(response => setUsers(response.data));
```

---

### 🔹 12.8 Building React CRUD Interface
- Build components for:
  - Displaying users
  - Adding a new user (form + POST)
  - Editing (form + PUT)
  - Deleting (button + DELETE)

---

Would you like a **ready Notion block**, a **starter Laravel API + React GitHub repo**, or **exercises** to go with this module? Let me know — I can prep those for you too.
