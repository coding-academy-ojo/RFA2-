# 🧱 Module 2: MVC Architecture in Laravel

## 🎯 Task: Build a Simple Blog Using MVC Pattern

### Objective
Apply MVC (Model-View-Controller) principles by creating a static blog with posts displayed via controller and view.

### ✅ Requirements

1. **Create a Controller**
   - Generate a `PostController`:
     ```bash
     php artisan make:controller PostController
     ```
   - Add an `index()` method that returns a view and passes sample blog data:
     ```php
     public function index()
     {
         $posts = [
             ['id' => 1, 'title' => 'Getting Started with Laravel', 'body' => 'Laravel is a powerful PHP framework...'],
             ['id' => 2, 'title' => 'Why MVC Matters', 'body' => 'MVC separates logic from presentation...']
         ];
         return view('posts.index', compact('posts'));
     }
     ```

2. **Create Blade Views**
   - Create `resources/views/posts/index.blade.php`
   - Extend a layout (create `layouts/app.blade.php` if needed)
   - Display all posts in a clean list with titles and excerpts

3. **Set Up Routes**
   - In `routes/web.php`:
     ```php
     use App\Http\Controllers\PostController;
     Route::get('/posts', [PostController::class, 'index']);
     ```

4. **Add a Show Page (Optional)**
   - Add a `show($id)` method to display one post by ID
   - Pass the selected post to `show.blade.php`

5. **Follow MVC Best Practices**
   - No logic in views
   - Controller handles data, view handles display

### 📦 Deliverables
- GitHub repo with:
  - `PostController.php`
  - Blade views in `resources/views/posts/`
  - Routes defined
  - `README.md` explaining the MVC flow

### 💡 Tip
Use `dd($posts)` to debug data flow from controller to view.