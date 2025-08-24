# 🏠 On-Demand Home Services Platform with React.js  

---

## 📝 Short Brief  
Students will build a **fully functional On-Demand Home Services Platform** using **React.js (App Router)** and **Redux Toolkit** for state management. The platform will connect customers with service providers (e.g., plumbers, electricians, cleaners) and allow users to **book services, make payments, and leave reviews**. The system will have **role-based access** for customers, service providers, and admins.  

---

## 🧰 Tech Competencies Acquired  
By completing this project, students will demonstrate proficiency in:  

- Structuring a **full-stack app** using **React.js (App Router)** and API routes.  
- Writing **modular, reusable components** with React Hooks (`useState`, `useEffect`, `useContext`).  
- Managing complex application state with **Redux Toolkit** (slices, thunks, DevTools).  
- Integrating **secure online payments** with Stripe or PayPal.  
- Implementing **ratings & reviews system** for services and providers.  
- Protecting routes with **role-based authentication** (JWT, httpOnly cookies).  
- Building **responsive UI** with Tailwind CSS or Bootstrap.  
- Using **Git/GitHub** for version control & collaboration.  
- Writing **professional project documentation** & README.  

---

## ✅ Project Requirements  

### 🔁 **Redux Toolkit Integration**  
- Create slices for:  
  - **Authentication** (Login/Logout, Current User)  
  - **Services** (List, Filter, Book, Cancel)  
  - **Bookings** (Pending, Completed, Canceled)  
  - **Payments** (Process, History)  
  - **Reviews** (Add, Edit, Delete)  
- Use **Redux Thunk** or **RTK Query** for API calls.  
- Maintain clean folder structure: `store/`, `slices/`, `api/`.  

---

### 👥 User Roles & Responsibilities  
- **Customer:** Browse services, book & pay, leave ratings & reviews.  
- **Service Provider:** Manage service listings, accept/decline bookings, view ratings.  
- **Admin:** Approve service providers, manage disputes, view analytics.  

---

### 🧱 Pages & Features  
- **Landing Page** (service categories, search, top-rated providers)  
- **Login / Register** (role selection during signup)  
- **Service Listings** (filter by category, rating, location)  
- **Booking Page** (select date/time, process payment)  
- **My Bookings** (view, reschedule, cancel)  
- **Provider Dashboard** (manage services, bookings)  
- **Admin Dashboard** (analytics, provider management)  

---

### 🔐 Role-Based Auth + JWT  
- Secure routes for each role.  
- JWT token handling with refresh support (optional).  
- Store tokens securely (httpOnly cookies).  

---

### 📈 Reports & Analytics  
- Admin dashboard showing:  
  - Total bookings & revenue  
  - Top service categories  
  - Provider performance ratings  

---

## 🎯 Performance Criteria  

| Criteria | Weight | Excellent (🏆) | Very Good (👍🏻) | Satisfactory (🔶) | Needs Improvement (❌) |
| --- | --- | --- | --- | --- | --- |
| ✅ Feature Completion | 25% | All features functional | Most functional | Some functional | Many missing |
| 💻 Code Quality | 15% | Modular, reusable | Some reuse | Messy/monolithic | Poor structure |
| 🔁 Redux Integration | 15% | Slices, thunks, DevTools used well | Minor logic issues | Basic state only | No proper Redux usage |
| 🔐 Auth & Role Mgmt | 10% | Secure & role-based | Mostly functional | Minor issues | Not implemented |
| 🎨 UI/UX | 10% | Polished & responsive | Good, minor issues | Basic UI | Broken layout |
| ⚙️ Functional Logic | 10% | Works end-to-end | Minor bugs | Some bugs | Major issues |
| 📁 Git & Collaboration | 5% | Clear commits | Minor inconsistencies | Disorganized | No commit structure |
| 📝 Documentation | 5% | Complete README | Basic README | Lacking details | Missing |

---

## 📦 Deliverables  
- GitHub repo with:  
  - Full source code using **React.js + Redux Toolkit**.  
  - Organized folder structure.  
  - `README.md` with setup, features, screenshots/video.  
- Trello board for task tracking.  
- Presentation slides for demo day.  

---

## 🚀 Improvements (Bonus)  
- AI-based **service recommendation system** based on user history.  
- **WebSocket notifications** for booking updates.  
- **Redux state persistence** with `redux-persist`.  
- **Service availability calendar** integration.  
