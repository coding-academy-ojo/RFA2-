# 🔗 Module 10: Advanced Eloquent Relationships in Laravel

## 🎯 Task: Add Categories and Tags to Tasks Using Eloquent Relationships

### Objective
Enhance the task system by adding categories and tags using one-to-many and many-to-many relationships.

### ✅ Requirements

1. **One-to-Many: Task Category**
   - Create `Category` model and migration:
     ```bash
     php artisan make:model Category -m
     ```
   - Fields: `name`, `user_id` (so users manage their own categories)
   - Relationship: `User → Categories → Tasks`

2. **Update Task Model**
   - Add `category_id` to tasks migration
   - Define relationships:
     ```php
     // Task.php
     public function category() { return $this->belongsTo(Category::class); }

     // Category.php
     public function tasks() { return $this->hasMany(Task::class); }
     ```

3. **Many-to-Many: Task Tags**
   - Create `Tag` model and pivot table:
     ```bash
     php artisan make:model Tag -m
     php artisan make:migration create_task_tag_table --create=task_tag
     ```
   - Use `attach()`, `detach()`, `sync()` in controller

4. **Update Task Form**
   - Dropdown to select category
   - Multi-select or chips input for tags

5. **Display Relationships**
   - Show category badge and tag list on task cards
   - Example: `<span>{{ $task->category->name }}</span>`

6. **Eager Loading**
   - Prevent N+1 queries:
     ```php
     $tasks = auth()->user()->tasks()->with('category', 'tags')->get();
     ```

### 📦 Deliverables
- GitHub repo with:
  - Two new models: `Category`, `Tag`
  - Migrations and relationships
  - Updated task form and display
  - `README.md` explaining relationship types used

### 💡 Tip
Mastering Eloquent relationships is key to building complex, scalable applications — this is a top skill for Laravel developers.