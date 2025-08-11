# 🔐 Module 6: CRUD Operations in Laravel

## 🎯 Task: Build a Full CRUD Interface for Tasks with Proper Validation

### Objective
Implement complete Create, Read, Update, and Delete (CRUD) functionality for tasks, ensuring data integrity and user feedback.

### ✅ Requirements

1. **Create Task Form**
   - Add a form on the dashboard to create new tasks
   - Fields: `title` (required), `description` (optional), `is_completed` (checkbox)
   - Use Laravel Blade forms with CSRF protection

2. **Store Task in Database**
   - In `TaskController@store`, validate input:
     ```php
     $request->validate([
         'title' => 'required|string|max:255',
         'description' => 'nullable|string',
     ]);
     ```
   - Save task with `user_id` (associate to logged-in user)

3. **Display All Tasks**
   - On the dashboard, list all tasks belonging to the authenticated user
   - Show title, description, completion status, and action buttons

4. **Edit & Update Task**
   - Add "Edit" button → opens a form pre-filled with task data
   - Use `TaskController@edit` and `@update`
   - Re-apply validation in `update` method

5. **Delete Task**
   - Add "Delete" button with confirmation
   - Use `DELETE` route and `TaskController@destroy`
   - Redirect back with success message

6. **User Feedback**
   - Use Laravel sessions to display status messages:
     ```php
     return redirect()->back()->with('success', 'Task updated!');
     ```
   - Display messages in Blade using `@if(session('success'))`

### 📦 Deliverables
- GitHub repo with:
  - Fully functional CRUD for tasks
  - Validated forms
  - Proper routes in `web.php`
  - `README.md` explaining CRUD flow and validation

### 💡 Tip
Use `php artisan route:list` to verify all CRUD routes are correctly defined.