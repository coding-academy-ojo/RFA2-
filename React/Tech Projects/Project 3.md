# 🎓 AI-Assisted Learning Management System (LMS) with React.js  

---

## 📝 Short Brief  
Students will build a **Learning Management System (LMS)** using **React.js (App Router)** and **Redux Toolkit** with **AI-powered learning assistance**. The platform will allow instructors to create courses, students to enroll, and AI to **generate quizzes, recommend content, and assist with grading**. Includes **secure payments** for premium courses and ratings & reviews for courses/instructors.  

---

## 🧰 Tech Competencies Acquired  
By completing this project, students will:  
- Structure a **full-stack LMS** using **React.js (App Router)** and API routes.  
- Write **reusable components** for courses, quizzes, dashboards.  
- Manage complex state using **Redux Toolkit** (slices, thunks, DevTools).  
- Integrate **AI features** via OpenAI API (quiz generation, content suggestions).  
- Implement **secure payments** with Stripe/PayPal.  
- Build a **ratings & feedback system** for courses and instructors.  
- Protect pages with **role-based authentication** (JWT, cookies).  
- Use **charting libraries** for analytics.  
- Collaborate with **Git/GitHub**.  

---

## ✅ Project Requirements  

### 🔁 **Redux Toolkit Integration**  
- Slices for:  
  - **Authentication** (Students, Instructors, Admins)  
  - **Courses** (List, Enroll, Update)  
  - **Quizzes** (Create, Take, Auto-Grade)  
  - **Payments** (Process, History)  
  - **Reviews** (Add, Edit, Delete)  
- Use **Redux Thunk** or **RTK Query** for API calls.  

---

### 👥 User Roles & Responsibilities  
- **Student:** Browse courses, enroll, take quizzes, submit feedback.  
- **Instructor:** Create courses, quizzes, view student progress.  
- **Admin:** Manage users, approve instructors, view reports.  

---

### 🧱 Pages & Features  
- **Landing Page** (featured courses, top instructors)  
- **Login / Register** (role selection)  
- **Course Listing & Details**  
- **Course Player** (video lessons, reading material)  
- **Quiz Generator** (AI-generated questions)  
- **Payment Page** (premium course purchase)  
- **Ratings & Reviews** for courses  
- **Dashboards** for each role  

---

### 🔐 Role-Based Auth + JWT  
- Secure page access per role.  
- Refresh token handling (optional).  
- Store tokens securely (httpOnly cookies).  

---

### 📈 Reports & Analytics  
- Admin dashboard: total users, revenue, top courses.  
- Instructor dashboard: student performance & course ratings.  

---

## 🎯 Performance Criteria  

| Criteria | Weight | Excellent (🏆) | Very Good (👍🏻) | Satisfactory (🔶) | Needs Improvement (❌) |
| --- | --- | --- | --- | --- | --- |
| ✅ Feature Completion | 25% | All features functional | Most functional | Some functional | Many missing |
| 💻 Code Quality | 15% | Modular, reusable | Some reuse | Messy/monolithic | Poor structure |
| 🔁 Redux Integration | 15% | Slices, thunks, DevTools used well | Minor issues | Basic state only | No Redux |
| 🔐 Auth & Role Mgmt | 10% | Secure & role-based | Mostly functional | Minor issues | Not implemented |
| 🎨 UI/UX | 10% | Polished & responsive | Good, minor issues | Basic UI | Broken layout |
| ⚙️ Functional Logic | 10% | Works end-to-end | Minor bugs | Some bugs | Major issues |
| 📁 Git & Collaboration | 5% | Clear commits | Minor inconsistencies | Disorganized | No commit structure |
| 📝 Documentation | 5% | Complete README | Basic README | Lacking details | Missing |

---

## 📦 Deliverables  
- GitHub repo with:  
  - Full source code using **React.js + Redux Toolkit**.  
  - Structured folders.  
  - `README.md` with setup instructions, features, and screenshots/video.  
- Trello board with tasks.  
- Presentation slides for demo day.  

---

## 🚀 Improvements (Bonus)  
- AI-powered **study assistant chatbot**.  
- **AI-driven personalized course recommendations**.  
- **Gamification features** (badges, leaderboards).  
- **Real-time Q&A board** with WebSocket support.  
