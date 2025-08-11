# 📦 Module 7: Form Validation & Handling in Laravel

## 🎯 Task: Enhance Form Validation and Error Handling

### Objective
Improve user experience by implementing robust server-side validation, custom error messages, and secure form handling.

### ✅ Requirements

1. **Advanced Validation Rules**
   - Update validation in `store` and `update` methods to include:
     ```php
     'title' => 'required|string|max:255|unique:tasks,title,NULL,id,user_id,' . auth()->id(),
     'description' => 'nullable|string|min:10|max:1000',
     'due_date' => 'nullable|date|after_or_equal:today',
     ```
   - Prevent duplicate task titles per user

2. **Custom Error Messages**
   - Pass custom messages to `validate()`:
     ```php
     $request->validate([...], [
         'title.unique' => 'You already have a task with this title.',
         'description.min' => 'Description must be at least 10 characters.'
     ]);
     ```

3. **Display Validation Errors**
   - In Blade, show errors using Laravel’s `$errors` variable:
     ```blade
     @error('title')
         <span class="text-red-500">{{ $message }}</span>
     @enderror
     ```

4. **Secure Form Handling**
   - Use Laravel’s `old()` helper to repopulate forms on error:
     ```blade
     <input name="title" value="{{ old('title') }}">
     ```
   - Handle file uploads securely (if adding due_date or attachments)

5. **Test Edge Cases**
   - Try submitting empty title, long description, past due date
   - Ensure proper error messages appear

### 📦 Deliverables
- GitHub repo with:
  - Enhanced validation logic
  - Custom error messages
  - Proper error display in Blade
  - `README.md` showing validation rules and UX improvements

### 💡 Tip
Validation is your app’s first line of defense — always validate on the server, even if you use JavaScript on the front.