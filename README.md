# 📋 ExamPortal

A fully client-side, browser-based exam portal built with HTML, CSS, and JavaScript. No backend or server required — all data is stored in `localStorage`.

---

## 🚀 Features

### 👤 Authentication
- Role-based login — **Student** and **Admin** roles
- Sign-up support with role selection
- Session persistence via `localStorage`

### 🎓 Student
- View available exams with subject, duration, marks, and description
- Attempt exams with a live countdown timer
- Support for three question types:
  - **MCQ** — Multiple choice with auto-grading
  - **FILL** — Fill-in-the-blank with auto-grading
  - **SHORT** — Short answer, manually evaluated by admin
- View detailed result with score breakdown and answer review
- Dashboard showing total exams, attempted, and remaining

### 🛡️ Proctoring System
- Detects tab switching / window focus loss
- 3-warning system before auto-submission
- 10-second countdown on each warning
- Warning count persists across accidental refresh

### 🔧 Admin Panel
- **Dashboard Overview** — Total exams, students, submissions, and pending evaluations
- **Manage Exams** — Create, edit, and delete exams; set duration, marks, passing marks, and negative marking
- **Questions** — Add/edit/delete questions per exam (MCQ, FILL, SHORT)
- **Subjects** — Create and manage subject categories
- **Evaluate Answers** — Manually grade short-answer responses with marks and feedback
- **Results** — View all student submissions and scores
- **Students** — View registered student list

### 📊 Result Page
- Score and percentage display
- Pass/Fail status
- Pending notice if short-answer questions are awaiting evaluation
- Full answer review with correct answers highlighted

---

## 🗂️ Project Structure

```
exam-portal-enhanced/
│
├── index.html          # Login & sign-up page
├── dashboard.html      # Student dashboard
├── exam.html           # Exam-taking interface
├── result.html         # Result & review page
├── admin.html          # Admin panel (all admin features)
│
├── js/
│   └── app.js          # Core logic: auth, DB helpers, exam engine, scoring
│
└── backend/            # (placeholder / future use)
```

---

## 📦 Preloaded Exam Data

The portal ships with **8 demo exams** covering:

| # | Exam | Questions | Type |
|---|------|-----------|------|
| 1 | General Knowledge | 25 | MCQ |
| 2 | Science & Technology | 25 | MCQ |
| 3 | Mathematics | 25 | MCQ |
| 4 | Logical Reasoning | 25 | MCQ |
| 5 | History & Geography | 20 | MCQ |
| 6 | English & Vocabulary | 20 | MCQ |
| 7 | Mixed Types Demo | Mixed | MCQ + FILL + SHORT |
| 8 | Java Programming | 20 | FILL + SHORT |

---

## 🔑 Default Credentials

| Role | Email | Password |
|------|-------|----------|
| Admin | `admin@examportal.com` | `Admin@123` |
| Student | `Shubham@student.com` | `Student@123` |

> You can register new student accounts from the login page.

---

## 🛠️ Tech Stack

- **HTML5** — Semantic structure
- **CSS3** — Custom design tokens, responsive layout (no framework)
- **Vanilla JavaScript** — All logic, routing, and state management
- **localStorage** — Client-side data persistence (no backend required)
- **Google Fonts** — Outfit & DM Sans

---

## ▶️ Getting Started

Since this is a pure frontend project, no installation or build step is needed.

1. **Clone or download** this repository
2. Open `index.html` in any modern browser
3. Log in with the default credentials above

```bash
git clone https://github.com/your-username/exam-portal.git
cd exam-portal
# Just open index.html in your browser
```

> For a better experience, serve it with a local server (e.g. VS Code Live Server or `npx serve .`).

---

## ⚠️ Limitations

- All data is stored in the browser's `localStorage` — clearing browser data will reset everything
- Not suitable for production use without a real backend and database
- No email verification or password hashing (demo/prototype only)

---

## 📄 Author

Shubham Kumar

## 📄 License

This project is created for educational and learning purposes.
