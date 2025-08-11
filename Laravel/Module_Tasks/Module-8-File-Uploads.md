# 🗂️ Module 8: File Uploads in Laravel

## 🎯 Task: Add Profile Picture Upload to User Account

### Objective
Allow users to upload and store a profile picture, learning secure file handling and storage in Laravel.

### ✅ Requirements

1. **Add `avatar` Field to Users Table**
   - Create a migration:
     ```bash
     php artisan make:migration add_avatar_to_users_table --table=users
     ```
   - Add: `$table->string('avatar')->nullable();`

2. **Update User Model**
   - Add `avatar` to fillable array:
     ```php
     protected $fillable = ['name', 'email', 'password', 'avatar'];
     ```

3. **Create Profile Edit Form**
   - Add a form on the dashboard to upload a profile picture
   - Include `enctype="multipart/form-data"`

4. **Handle File Upload**
   - In controller, validate and store:
     ```php
     if ($request->hasFile('avatar')) {
         $path = $request->file('avatar')->store('avatars', 'public');
         $user->avatar = $path;
     }
     ```
   - Use `public` disk in `config/filesystems.php`

5. **Display Uploaded Image**
   - Use `asset('storage/' . $user->avatar)` in Blade
   - Create symbolic link:
     ```bash
     php artisan storage:link
     ```

6. **Validation & Security**
   - Validate: `'avatar' => 'nullable|image|max:2048|mimes:jpg,png,jpeg'`
   - Delete old avatar when uploading new one (optional bonus)

### 📦 Deliverables
- GitHub repo with:
  - Migration for `avatar` field
  - File upload logic
  - Profile form with image preview
  - `README.md` explaining file storage setup

### 💡 Tip
Never store uploads in `public/` directly — use Laravel’s storage system with `php artisan storage:link` for security.