# 🏥 Hospital Management System with React.js  

---

## 📝 Short Brief  
Students will build a **fully functional Hospital Management System** using **React.js (App Router)** and **Redux Toolkit** to manage global state. This system will allow users to interact securely through **role-based access** and perform tasks such as managing appointments, billing, patient records, and generating analytics reports. This project serves as a **comprehensive application** of everything learned in the React module.  

---

## 🧰 Tech Competencies Acquired  
By completing this project, students will demonstrate proficiency in:  

- Structuring a **full-stack app** using **React.js (App Router)** and API routes.  
- Writing **modular, reusable components** using React Hooks (`useState`, `useEffect`, `useContext`).  
- Managing complex application state using **Redux Toolkit**.  
- Setting up **Redux slices**, **async thunks**, and **Redux DevTools**.  
- Navigating pages using the **React Router** layout system.  
- Creating and consuming **RESTful APIs** for CRUD operations.  
- Handling **authentication** using JWT and protecting routes by roles.  
- Designing responsive UI using **Tailwind CSS**, **Bootstrap**, or custom styles.  
- Using **Git/GitHub** for version control and collaboration.  
- Writing professional-level **README** and project documentation.  

---

## ✅ Project Requirements  

### 🔁 **Redux Toolkit Integration**  
- Set up **global state management** using Redux Toolkit.  
- Organize slices for at least:  
  - **Authentication** (Login/Logout, Current User)  
  - **Appointments** (Create, Update, Cancel)  
  - **Patients** (Records, Medical History)  
  - **Billing** (Invoices, Payments)  
- Use **Redux Thunk** to handle async API calls.  
- Access state via `useSelector` and dispatch actions with `useDispatch`.  
- Maintain a clean folder structure: `store/`, `slices/`, and reusable action handlers.  

---

### 👥 User Roles & Responsibilities  
- **Admin:** Manage all hospital operations, staff, and reports.  
- **Healthcare Provider:** Manage patient records, appointments, and prescriptions.  
- **Patient:** View medical history, book appointments, and pay bills online.  

---

### 🧱 Pages & Features  
- **Landing Page** (overview & services)  
- **Login / Register** (role selection)  
- **Appointments Management** (book, update, cancel)  
- **Patient Records** (medical history, prescriptions)  
- **Billing & Payments** (online invoices)  
- **Dashboards** for each role  
- **Reports & Analytics** (admin only)  

---

### 🔐 Role-Based Auth + JWT  
- JWT token management with refresh support (optional).  
- Protect React.js pages using middleware or HOC for roles.  
- Store tokens securely (httpOnly cookies or localStorage with caution).  

---

### 📈 Reports & Analytics  
- Admin-only dashboard with:  
  - Number of patients & appointments  
  - Billing summaries  
  - Performance metrics for staff  

---

## 🎯 Performance Criteria  

| Criteria | Weight | Excellent (🏆) | Very Good (👍🏻) | Satisfactory (🔶) | Needs Improvement (❌) |
| --- | --- | --- | --- | --- | --- |
| ✅ Feature Completion | 25% | All key features work | Most work | Half work | Many missing |
| 💻 Code Quality | 15% | Modular, reusable | Some reuse | Messy/monolithic | Poor structure |
| 🔁 Redux Integration | 15% | Redux used effectively with slices, thunks | Minor logic issues | Basic state only | No proper Redux usage |
| 🔐 Auth & Role Mgmt | 10% | Secure & role-based | Mostly functional | Minor issues | Not implemented |
| 🎨 UI Design & UX | 10% | Fully responsive, polished | Good but needs refinement | Basic UI | Broken layout |
| ⚙️ Functional Logic | 10% | Works end-to-end | Minor bugs | Some logic bugs | Major issues |
| 📁 Git & Collaboration | 5% | Organized, team commits | Few inconsistencies | Disorganized | No clear commits |
| 📝 Documentation | 5% | Complete README + usage | Basic README | Lacking details | Missing |

---

## 📦 Deliverables  
- GitHub Repository with:  
  - Full source code using **React.js + Redux Toolkit**.  
  - Organized folder structure: `components/`, `pages/`, `store/`, `slices/`, `api/`.  
  - `README.md` covering:  
    - Tech stack (with Redux highlighted)  
    - Setup instructions  
    - Features list  
    - Screenshots/video demo (optional)  
- Trello board showing task assignments.  
- Presentation slides for demo day.  

---

## 🚀 Improvements (Bonus)  
- Persist Redux state using `redux-persist`.  
- Integrate custom middleware for logging or error handling.  
- Use **RTK Query** for data fetching instead of thunks.  
- Add WebSocket for real-time updates (appointments, notifications).  
- Add optimistic UI updates with Redux actions.  