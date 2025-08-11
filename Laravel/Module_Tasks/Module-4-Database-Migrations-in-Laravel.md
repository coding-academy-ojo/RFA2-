# 🗃️ Module 4: Database & Migrations in Laravel

## 🎯 Task: Design and Migrate a Posts Database

### Objective
Replace hardcoded data with a real database using Laravel migrations and Eloquent.

### ✅ Requirements

1. **Create a Migration for Posts**
   - Generate migration:
     ```bash
     php artisan make:migration create_posts_table --create=posts
     ```
   - Define fields: `title`, `body`, `published (boolean)`, `user_id`

2. **Run the Migration**
   - ```bash
     php artisan migrate
     ```

3. **Create a Post Model**
   - ```bash
     php artisan make:model Post
     ```
   - Add fillable fields:
     ```php
     protected $fillable = ['title', 'body', 'published', 'user_id'];
     ```

4. **Seed the Database**
   - Create a seeder:
     ```bash
     php artisan make:seeder PostSeeder
     ```
   - Insert 3 sample posts
   - Run:
     ```bash
     php artisan db:seed --class=PostSeeder
     ```

5. **Update Controller to Use Eloquent**
   - In `PostController@index`:
     ```php
     $posts = Post::all();
     ```

### 📦 Deliverables
- GitHub repo with:
  - Migration file
  - `Post` model
  - Seeder
  - Updated controller using Eloquent
  - `README.md` explaining the database schema

### 💡 Tip
Use `php artisan tinker` to test Eloquent queries interactively.