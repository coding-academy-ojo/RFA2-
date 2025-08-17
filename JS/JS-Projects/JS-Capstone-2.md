# JS Capstone Project 2

### **📛 Title**

## **PlanIt – Event Planner & Smart Reminder – SaaS Application**

---

### **📝 Short Brief**

PlanIt is a **browser-based SaaS platform** that helps individuals, teams, and organizations plan events, set reminders, and manage schedules in one place.

It simulates a **multi-user** environment where each account stores its own events, reminders, and tasks, and syncs them locally or via an API.

---

### **🛠 Tech Competencies Acquired**

By completing this project, learners will gain:

- **JavaScript Core Skills** – DOM manipulation, event listeners, ES6+ syntax, template literals.
- **Date & Time Handling** – Using JavaScript’s `Date` object, formatting, countdowns, and comparisons.
- **Data Persistence** – Storing and retrieving data from `localStorage` or a mock API.
- **Dynamic UI Creation** – Generating interactive event cards and schedules.
- **Search & Filter Features** – Finding events by date, category, or keyword.
- **Responsive Web Design** – Mobile-first layouts for event lists and calendars.
- **SaaS Product Thinking** – Structuring features for multiple users with separate dashboards.

---

### **🌍 Project Context**

From corporate meetings to personal celebrations, people need a **central hub** to keep track of upcoming events and important dates.

PlanIt will simulate this environment, giving learners experience in building **productivity-focused SaaS tools**.

The app will:

- Let users **sign in** and view only their events.
- Create, edit, and delete events with details (title, date, time, location, category).
- Set reminders that trigger notifications before the event.
- Organize events into **categories** (Work, Personal, Social, etc.).

---

### **📋 Project Requirements**

The application must include:

1. **User Login (Simulated)**
    - Basic sign-in with a username/email.
    - Separate event lists for each logged-in user.
2. **Event Management**
    - Add a new event with title, date, time, description, location, and category.
    - Edit and delete existing events.
3. **Reminders & Notifications**
    - Countdown timers to upcoming events.
    - Alert or pop-up notification at a set time before the event.
4. **Calendar View & Filtering**
    - Monthly/weekly calendar layout.
    - Filter events by date or category.
5. **Data Storage**
    - Store all event and reminder data in `localStorage`.
6. **Responsive Layout**
    - User-friendly on desktop, tablet, and mobile.

---

### **📊 Performance Criteria**

The project will be evaluated based on:

- **Functionality** – All event and reminder features work flawlessly.
- **Code Quality** – Modular structure, reusable functions, meaningful variable names.
- **UI/UX** – Clear layouts, easy navigation, and appealing design.
- **SaaS Simulation** – Data properly isolated for different users.
- **Extra Features** – Export events to CSV, dark mode, or recurring event scheduling.

---

### **🧪 Assessment Methods**

- **Live Demo** – Walkthrough from login to event creation and reminder notifications.
- **Code Review** – Checking for clean, readable, and efficient JavaScript.
- **Peer Testing** – Classmates test usability and give structured feedback.

---

## 🧭 Assessment Overview

Assessors should evaluate PlanIt on scheduling correctness, reliability of reminders, calendar UX, and durability of data persistence. Total points = **100**.

---

## 🧾 Rubric (Each row scored 1–4)

| Criterion (weight %) | Excellent (4) | Good (3) | Fair (2) | Poor (1) |
| --- | --- | --- | --- | --- |
| **Core Functionality (25%)** | Create/edit/delete events, reminders, categories, recurring options work flawlessly. | Most features implemented with small bugs. | Core flows work but missing key functions. | Several features missing or non-functional. |
| **Notifications & Reminders (20%)** | Reliable reminders (timers/alerts) with correct timing; supports configurable lead times. | Reminders mostly reliable; occasional timing issues. | Basic reminders present but flaky. | No functioning reminders. |
| **Calendar UI & Filtering (12%)** | Calendar view (monthly/weekly) + filters and quick jump-to-date are polished. | Calendar present with minor UX issues. | Calendar basic or limited view. | No calendar view. |
| **Data Persistence & Multi-User (12%)** | Data stored in localStorage per user; sessionStorage holds last viewed/calendar state. | Persistence works with minor edge cases. | Persistence inconsistent or mixed users. | No reliable persistence. |
| **Code Quality & Modularity (10%)** | Clean modules, documented code, reusable utilities for dates and storage. | Mostly clean with modest refactors needed. | Messy organization; limited documentation. | Unreadable or monolithic code. |
| **UX & Accessibility (8%)** | Responsive, easy to use, keyboard accessible, semantic markup. | Usable UI with some breakpoints issues. | Cluttered or limited mobile support. | Non-responsive and inaccessible. |
| **Error Handling (6%)** | Handles invalid dates, timezone issues, and offline behavior gracefully. | Basic error handling. | Errors surface as console logs only. | App crashes on invalid input. |
| **Bonus Features / Innovation (7%)** | Recurring events, CSV export, snooze options, timezone conversion. | Some bonuses implemented. | Attempted some but incomplete. | No extras. |

---

## ⚖️ Grading Scheme & Passing Thresholds

- Max score = **100**.
- Passing threshold = **72 / 100** (slightly higher due to time/date complexity).
- Grade bands:
    - **88–100** = Excellent (A)
    - **72–87** = Satisfactory (B)
    - **55–71** = Needs Improvement (C)
    - **<55** = Fail (D/F)

Weights as above used to compute total.

---

## ✅ Detailed Assessment Method (Trainer Guide)

**Preparation**

1. Pull the repo; follow README to run locally or on a test host.
2. Review instructions for setting reminder lead times/timezone handling.

**Functional Checklist**

- [ ]  Login simulation & per-user event lists.
- [ ]  Create event with title, date, start/end time, location, category.
- [ ]  Edit/delete events and confirm calendar updates.
- [ ]  Add reminder lead time (e.g., 10 min, 1 day); confirm alert fires.
- [ ]  Recurring events (if required): daily/weekly/monthly patterns and exceptions.
- [ ]  Calendar navigation: month/week/day views (if implemented).
- [ ]  Filter events by date/category/search.
- [ ]  Persistence across reload and correct last-view via sessionStorage.

**Notifications & Reminder Testing**

- [ ]  Test reminder firing by setting events a minute ahead and observing alert/notification.
- [ ]  Test snooze/reschedule behavior (if implemented).
- [ ]  Simulate browser closed + reopened: check persistence (reminder may not fire offline — note design limits).

**Edge Cases**

- [ ]  Timezone handling (if expected): create events under different timezone assumptions.
- [ ]  Invalid date handling (past dates, end < start).
- [ ]  Large number of events performance test (50–200 events).

**Code Review Checklist**

- [ ]  Clear division: calendar logic, reminder scheduler, storage layer.
- [ ]  Proper date utility usage or helper functions (avoid ad-hoc date math).
- [ ]  Comments explaining scheduling algorithm.
- [ ]  No secrets or API keys in repo.

**UX/Accessibility**

- [ ]  Keyboard flows for creating/editing events.
- [ ]  Semantic HTML for forms and ARIA roles for modal dialogs.
- [ ]  Responsive design verified on mobile and tablet sizes.

**Demo Scoring**

- Student performs a 7–10 minute demo: create an event, set reminder, show calendar, simulate reminder — trainers score per rubric.

<aside>
🤔

**Peer Testing →** still not sure whether to implement or not

- Peers attempt to create conflicting events and test notification behavior, recording any observed bugs.
</aside>

**Final Report**

- Trainer completes scoring sheet with numerical breakdown and written feedback (strengths, required fixes, optional improvements). Provide remediation tasks and deadlines if below passing.

---

## 🛠 Remediation & Resubmission Policy

- If score **<70**, compile a remediation plan (list of bugs / missing features) with priority and 2-5 days for resubmission.
- Allow resubmission after fixes; re-evaluation limited to the corrected areas. The maximum resubmission grade is capped at 80, unless major new features are added.

---

### **📦 Deliverables**

- Fully functional **Event Planner & Reminder SaaS app** (PlanIt).
- Complete source code with HTML, CSS, JavaScript, and any assets.
- README with setup instructions, feature list, and screenshots.
- Optional recorded demo video showing main features.
