<div align="center">

# 🏨 HotelHub

### *Laravel API + React Frontend Hotel Booking System*

![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![GitHub stars](https://img.shields.io/github/stars/yourusername/hotelhub?style=flat-square)](https://github.com/yourusername/hotelhub/stargazers)

**⏱️ Duration:** 10 Hours | **🎯 Difficulty:** Intermediate

---

</div>

## 🚀 Project Overview

Build **HotelHub** - a modern hotel booking system using a decoupled architecture. The backend is powered by a robust Laravel API, while the frontend is a dynamic React application. Manage rooms, handle bookings, and provide a seamless user experience.

### ✨ What You'll Build

<table>
<tr>
  <td align="center">
    <img src="https://img.icons8.com/fluency/48/000000/home.png" width="40"><br>
    <b>🏨 View Rooms</b><br>
    <sub>Display available rooms</sub>
  </td>
  <td align="center">
    <img src="https://img.icons8.com/fluency/48/000000/calendar-plus.png" width="40"><br>
    <b>📅 Book Rooms</b><br>
    <sub>Create new bookings</sub>
  </td>
  <td align="center">
    <img src="https://img.icons8.com/fluency/48/000000/edit-calendar.png" width="40"><br>
    <b>✏️ Manage Bookings</b><br>
    <sub>View & update bookings</sub>
  </td>
  <td align="center">
    <img src="https://img.icons8.com/fluency/48/000000/delete-sign.png" width="40"><br>
    <b>🗑️ Cancel Bookings</b><br>
    <sub>Handle cancellations</sub>
  </td>
</tr>
</table>

---

## 🏗️ Architecture & Models

### 🛏️ Room Model
> **🎯 Core Entity** - Represents a hotel room

```php
// Required Fillable Attributes
✅ id
✅ room_number
✅ type (e.g., Single, Double, Suite)
✅ price_per_night
✅ description
✅ is_available (boolean)
```

### 📅 Booking Model
> **📅 Transaction Entity** - Records guest bookings

```php
// Required Fillable Attributes
✅ id
✅ guest_name
✅ guest_email
✅ check_in_date
✅ check_out_date
✅ room_id (foreign key)
✅ status (e.g., Confirmed, Cancelled)
```

### 🔗 Relationships

*   `Room` has many `Bookings`.
*   `Booking` belongs to a `Room`.

---

## 🎮 Laravel API Controller Actions

<details>
<summary><b>🛏️ Rooms API Controller</b> - Click to expand</summary>

| 🎯 Method     | 📝 Description         | 🌐 Purpose                      |
|---------------|------------------------|---------------------------------|
| `index()`     | 📋 List all rooms      | Retrieve a list of rooms        |
| `store()`     | ➕ Create a room       | Add a new room                  |
| `show()`      | 👁️ Get a room         | Retrieve details of one room    |
| `update()`    | 🔄 Update a room       | Modify an existing room         |
| `destroy()`   | 🗑️ Delete a room       | Remove a room                   |

</details>

<details>
<summary><b>📅 Bookings API Controller</b> - Click to expand</summary>

| 🎯 Method     | 📝 Description         | 🌐 Purpose                      |
|---------------|------------------------|---------------------------------|
| `index()`     | 📋 List all bookings   | Retrieve a list of bookings     |
| `store()`     | ➕ Create a booking    | Add a new booking               |
| `show()`      | 👁️ Get a booking      | Retrieve details of one booking |
| `update()`    | 🔄 Update a booking    | Modify an existing booking      |
| `destroy()`   | 🗑️ Delete a booking    | Remove a booking                |

</details>

---

## 🛣️ Laravel RESTful API Endpoints

### 🛏️ **Rooms Endpoints**

| 🌐 Method | 📍 URI                  | 🎯 Action | 🏷️ Route Name       | 🎨 Description           |
|-----------|--------------------------|-----------|----------------------|---------------------------|
| `GET`     | `/api/rooms`             | `index`   | `api.rooms.index`    | Get all rooms             |
| `POST`    | `/api/rooms`             | `store`   | `api.rooms.store`    | Create a new room         |
| `GET`     | `/api/rooms/{room}`      | `show`    | `api.rooms.show`     | Get a specific room       |
| `PUT/PATCH`| `/api/rooms/{room}`     | `update`  | `api.rooms.update`   | Update a specific room    |
| `DELETE`  | `/api/rooms/{room}`      | `destroy` | `api.rooms.destroy`  | Delete a specific room    |

### 📅 **Bookings Endpoints**

| 🌐 Method | 📍 URI                   | 🎯 Action | 🏷️ Route Name        | 🎨 Description            |
|-----------|---------------------------|-----------|------------------------|---------------------------|
| `GET`     | `/api/bookings`           | `index`   | `api.bookings.index`   | Get all bookings          |
| `POST`    | `/api/bookings`           | `store`   | `api.bookings.store`   | Create a new booking      |
| `GET`     | `/api/bookings/{booking}` | `show`    | `api.bookings.show`    | Get a specific booking    |
| `PUT/PATCH`| `/api/bookings/{booking}`| `update`  | `api.bookings.update`  | Update a specific booking |
| `DELETE`  | `/api/bookings/{booking}` | `destroy` | `api.bookings.destroy` | Delete a specific booking |

---

## 🎨 React Frontend Components

### 📱 Key Views

<div align="center">

| 🏠 **Room List** | ➕ **Book Room** | 📅 **My Bookings** | 🛏️ **Room Details** |
|:----------------:|:----------------:|:------------------:|:-------------------:|
| 📊 Room Grid     | 📝 Booking Form  | 📋 Booking List    | 🔍 Room Details     |
| 🔍 Search/Filter | ✅ Validation    | ✏️ Edit Booking     | 🖼️ Room Images      |
| 📱 Responsive    | 🎨 Modern UI     | 🗑️ Cancel Booking   | 💰 Pricing Info     |

</div>

### 🧩 Core Components

*   `RoomList`: Fetches and displays available rooms.
*   `RoomDetails`: Shows detailed information for a specific room.
*   `BookingForm`: Allows users to create a new booking for a room.
*   `BookingList`: Displays a list of user bookings with options to view/edit/cancel.
*   `BookingDetails`: Shows detailed information for a specific booking.

---

## ⚡ Quick Start Guide

### 🚀 **Backend (Laravel API) Setup**

```bash
# 1️⃣ Clone the repository
git clone https://github.com/yourusername/hotelhub.git
cd hotelhub

# 2️⃣ Navigate to backend directory (if separate)
cd backend # or assume root is Laravel

# 3️⃣ Install Laravel dependencies
composer install

# 4️⃣ Environment setup
cp .env.example .env
php artisan key:generate

# 5️⃣ Database configuration (update .env)
# DB_CONNECTION=mysql
# DB_HOST=127.0.0.1
# DB_PORT=3306
# DB_DATABASE=hotelhub
# DB_USERNAME=your_username
# DB_PASSWORD=your_password

# 6️⃣ Run migrations
php artisan migrate

# 7️⃣ (Optional) Seed the database
php artisan db:seed

# 8️⃣ Serve the Laravel API
php artisan serve --port=8000
```

### 🚀 **Frontend (React App) Setup**

```bash
# 1️⃣ Navigate to frontend directory (in a new terminal)
cd ../frontend # or hotelhub-frontend if separate repo/folder

# 2️⃣ Install React dependencies
npm install

# 3️⃣ Configure API base URL (typically in a .env file or config)
# REACT_APP_API_BASE_URL=http://localhost:8000/api

# 4️⃣ Start the React development server
npm start
```

### ⚙️ **Database Configuration (.env)**

Update your Laravel `.env` file with your database credentials:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=hotelhub
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

---

## 📁 Project Structure (Simplified)

```
🏗️ HotelHub/
├── 📁 backend/ (Laravel API)
│   ├── 📱 app/
│   │   ├── 🎯 Models/
│   │   │   ├── 🛏️ Room.php
│   │   │   └── 📅 Booking.php
│   │   └── 🎮 Http/Controllers/Api/
│   │       ├── 🛏️ RoomController.php
│   │       └── 📅 BookingController.php
│   ├── 🛣️ routes/
│   │   └── api.php # Define your API routes here
│   └── 🗄️ database/migrations/
└── 📁 frontend/ (React App)
    ├── 📁 src/
    │   ├── 🧩 components/
    │   │   ├── 🛏️ RoomList.js
    │   │   ├── 🛏️ RoomDetails.js
    │   │   ├── 📅 BookingForm.js
    │   │   ├── 📅 BookingList.js
    │   │   └── 📅 BookingDetails.js
    │   ├── 🌐 services/
    │   │   └── api.js # Axios calls to Laravel API
    │   ├── 🎨 App.js
    │   └── 🎨 index.js
    └── package.json
```

---

## ✨ Features Showcase

<div align="center">

### 🎯 **Core Features**

| Feature                     | Status | Description                                |
|-----------------------------|:------:|--------------------------------------------|
| 🛏️ **Room Management API**  | ✅     | CRUD operations for hotel rooms (Backend)  |
| 📅 **Booking Management API**| ✅     | CRUD operations for guest bookings (Backend)|
| 🛣️ **RESTful API Endpoints**| ✅     | Standardized backend communication         |
| 🔗 **API Data Relationships**| ✅     | Proper data linking (Room-Bookings)        |
| 🗄️ **Database Migrations**  | ✅     | Structured database schema                 |
| ✅ **API Validation**        | ✅     | Request data validation (Backend)          |
| 🎨 **React UI**             | ✅     | Interactive frontend for users             |
| 📱 **Responsive Design**    | ✅     | Works on desktop and mobile                |
| 🔐 **Basic Security**       | ✅     | Secure API practices                       |

</div>

---

## 🛠️ Tech Stack

<div align="center">

### **Backend Powerhouse**
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)

### **Frontend Magic**
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)

### **API Communication**
![Axios](https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white)
![JSON](https://img.shields.io/badge/JSON-000000?style=for-the-badge&logo=json&logoColor=white)

</div>

---

## 🎯 Learning Objectives

<table>
<tr>
<td width="50%">

### 🧠 **Skills You'll Master**
- ✅ Laravel API Development
- ✅ RESTful API Design
- ✅ Eloquent ORM Relationships
- ✅ React Component Architecture
- ✅ State Management (useState, useEffect)
- ✅ Making API Calls (Axios/Fetch)

</td>
<td width="50%">

### 🚀 **Best Practices**
- ✅ Decoupled Frontend & Backend
- ✅ Consistent API Contracts
- ✅ Responsive UI Design
- ✅ Form Handling & Validation (FE/BE)
- ✅ Error Handling (Client & Server)
- ✅ Clean Project Structure

</td>
</tr>
</table>

---

## 🤝 Contributing

<div align="center">

We love your input! We want to make contributing as easy and transparent as possible.

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=for-the-badge)](http://makeapullrequest.com)
[![GitHub issues](https://img.shields.io/github/issues/yourusername/hotelhub?style=for-the-badge)](https://github.com/yourusername/hotelhub/issues)

**Ways to contribute:**
- 🐛 Report bugs
- 💡 Suggest features
- 📝 Improve documentation
- 🔧 Submit pull requests

</div>

---

## 📄 License

<div align="center">

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

</div>

---

<div align="center">

### 🌟 **Show Your Support**

Give a ⭐️ if this project helped you learn full-stack development!

**🎬 Made with ❤️ and lots of ☕ by [OrangeAcademyTeam]**


[![GitHub followers](https://img.shields.io/github/followers/yourusername?style=social)](https://github.com/yourusername)
[![Twitter Follow](https://img.shields.io/twitter/follow/yourusername?style=social)](https://twitter.com/yourusername)

---

*Happy Coding! 🚀*

</div>