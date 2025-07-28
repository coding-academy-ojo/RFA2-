# Larastore - Laravel CRUD Application

**Duration:** 5 Hours

## Overview

Create an online store to manage Products. This application should contain 3 main pages:
- View Products
- Add Products  
- Update Products

*Note: Remove Products is just an action without a dedicated page.*

## Requirements

### 1. Create the Product Model

Create a Model called `Product` following Laravel framework naming conventions. The Product model must include the **fillable attribute** with the following fields:

- `id`
- `product_name`
- `product_description`
- `product_price`

### 2. Create the Products Controller

Create a Products Controller that includes all basic CRUD methods:

1. **index**: Redirect user to the landing page
2. **create**: Create a new product (redirect to the related view page)
3. **store**: Store the product data coming from the view
4. **edit**: Update a specific product (redirect to the related view page)
5. **update**: Store the updated values
6. **destroy**: Delete a product

#### Products Routes Table

| Verb      | URI                    | Action  | Route Name      |
|-----------|------------------------|---------|-----------------|
| GET       | /products              | index   | products.index  |
| GET       | /products/create       | create  | products.create |
| POST      | /products              | store   | products.store  |
| GET       | /products/{product}    | show    | products.show   |
| GET       | /products/{product}/edit | edit  | products.edit   |
| PUT/PATCH | /products/{product}    | update  | products.update |
| DELETE    | /products/{product}    | destroy | products.destroy|

### 3. Create the Categories Model

Create a Model called `Category` following Laravel framework naming conventions. The Category model must include the **fillable attribute** with the following fields:

- `id`
- `category_name`
- `category_description`

### 4. Create the Categories Controller

Create a Categories Controller that includes all basic CRUD methods:

1. **index**: Redirect user to the main category page
2. **create**: Create a new category (redirect to the related view page)
3. **store**: Store the category data coming from the view
4. **edit**: Update a specific category (redirect to the related view page)
5. **update**: Store the updated values
6. **destroy**: Delete a category

#### Categories Routes Table

| Verb      | URI                        | Action  | Route Name        |
|-----------|----------------------------|---------|-------------------|
| GET       | /categories                | index   | categories.index  |
| GET       | /categories/create         | create  | categories.create |
| POST      | /categories                | store   | categories.store  |
| GET       | /categories/{category}     | show    | categories.show   |
| GET       | /categories/{category}/edit| edit    | categories.edit   |
| PUT/PATCH | /categories/{category}     | update  | categories.update |
| DELETE    | /categories/{category}     | destroy | categories.destroy|

### 5. Create the Related Views

Create four pages for the CRUD application:

1. **Index Page**: Data grid showing records from the products database table with actions for each record (view details, update, delete)
2. **Create Page**: Form for creating new products
3. **Edit Page**: Form for updating existing products
4. **Show Page**: Display individual product details

Include a **Create** button on top of the data grid for creating new records in the products table.

### 6. Create Data Migrations

Create database migrations using Laravel's artisan commands. The database schema should match the model attributes.

**Important Requirements:**
- Database tables should be plural
- **DO NOT create tables manually**
- Use Laravel migrations only

### 7. Configure Environment

Edit the `.env` file with all database connection information:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=larastore
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

### 8. Define Model Relationships

Edit the model files to establish proper relationships between Products and Categories.

### 9. Update Migration Files

Edit the migration files to ensure relationships are properly defined in the database schema.

## Getting Started

1. Clone the repository
2. Run `composer install`
3. Copy `.env.example` to `.env` and configure database settings
4. Run `php artisan migrate`
5. Run `php artisan serve`

## Project Structure

```
app/
├── Models/
│   ├── Product.php
│   └── Category.php
├── Http/Controllers/
│   ├── ProductController.php
│   └── CategoryController.php
resources/views/
├── products/
│   ├── index.blade.php
│   ├── create.blade.php
│   ├── edit.blade.php
│   └── show.blade.php
└── categories/
    ├── index.blade.php
    ├── create.blade.php
    ├── edit.blade.php
    └── show.blade.php
```

## Features

- ✅ Full CRUD operations for Products
- ✅ Full CRUD operations for Categories
- ✅ RESTful routing
- ✅ Model relationships
- ✅ Database migrations
- ✅ Responsive views
- ✅ Form validation

## Technologies Used

- Laravel Framework
- PHP
- MySQL
- Blade Templates
- Bootstrap (optional for styling)# RFA2-