# 🎨 Module 3: Blade Templating

## 🎯 Task: Design a Reusable Layout with Blade Components

### Objective
Master Blade templating by creating a consistent, responsive layout with components and inheritance.

### ✅ Requirements

1. **Create a Master Layout**
   - File: `resources/views/layouts/app.blade.php`
   - Include:
     - `<head>` with title
     - Navigation menu (Home, Posts, About)
     - Main content section: `@yield('content')`
     - Footer

2. **Use Layout Inheritance**
   - Update `posts/index.blade.php` to extend the layout:
     ```blade
     @extends('layouts.app')
     @section('content')
         <h1>Blog Posts</h1>
         <!-- posts list -->
     @endsection
     ```

3. **Create a Blade Component**
   - Make a `CardComponent` for blog posts:
     ```bash
     php artisan make:component PostCard
     ```
   - Use it in `index.blade.php`:
     ```blade
     @foreach($posts as $post)
         <x-post-card :post="$post" />
     @endforeach
     ```

4. **Add Conditional Styling**
   - In `PostCard`, highlight the first post with a different background using `@if($loop->first)`

5. **Responsive Design**
   - Use Tailwind CSS or simple CSS to make the layout mobile-friendly

### 📦 Deliverables
- GitHub repo with:
  - `layouts/app.blade.php`
  - `PostCard` component
  - Updated views using components and `@extends`
  - `README.md` showing how Blade improves reusability

### 💡 Tip
Blade components make UI consistent — perfect for buttons, cards, and forms.