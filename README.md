# CampusSync-Capstone_Project
MERN-based ERP that unifies admissions, fees, hostel, exams &amp; library in one student database. Features role-based access, automated fee receipts and real-time admin dashboards. Low-cost, cloud-ready alternative to expensive ERP suites
<div align="center">

# 🎓 CampusSync

### One Student. One Database. One Counter.

**An affordable, cloud-ready ERP for integrated student management**

![SIH 2025](https://img.shields.io/badge/SIH-2025-orange?style=for-the-badge)
![PS ID](https://img.shields.io/badge/PS%20ID-SIH25103-blue?style=for-the-badge)
![Stack](https://img.shields.io/badge/Stack-MERN-success?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=for-the-badge)

![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)

</div>

---

## 📌 Problem Statement

| Field | Details |
|---|---|
| **Hackathon** | Smart India Hackathon 2025 |
| **PS ID** | SIH25103 |
| **Title** | ERP-based Integrated Student Management System |
| **Organization** | Government of Rajasthan |
| **Category** | Software |
| **Theme** | Smart Automation |
| **Domain** | Education / Student Management |

Admissions, fee collection, hostel allocation, examination and library records are usually kept in **separate ledgers and systems**. Students visit multiple counters, staff enter the same data again and again, and administrators have **no real-time consolidated view** of the institution. Comprehensive ERP suites exist, but many institutions cannot afford them.

---

## 💡 Our Solution

**CampusSync** brings every student-facing process into **one centralized database** built on the MERN stack and widely available cloud services. No expensive proprietary software, no hardware-heavy setup.

```
                ┌──────────────────────────────┐
                │      Central Student DB      │
                │   (MongoDB Atlas, 1 record)  │
                └──────────────┬───────────────┘
        ┌───────────┬──────────┼──────────┬───────────┐
        ▼           ▼          ▼          ▼           ▼
   Admissions     Fees       Hostel     Exams      Library
        └───────────┴──────────┼──────────┴───────────┘
                               ▼
                   Real-time Admin Dashboard
```

---

## ✨ Key Features

| Module | What it does |
|---|---|
| 🔐 **Auth & Roles** | JWT login with role-based access (Admin, Officer, Accountant, Warden, Exam Cell, Librarian, Student) |
| 📝 **Admissions** | Online application, document upload, verification and approval workflow |
| 💰 **Fee Management** | Fee structure, online payment, **automated PDF receipts**, dues tracking |
| 🏠 **Hostel** | Room allocation, vacancy tracking, allotment history |
| 📚 **Library** | Book issue/return, fines, availability, linked to the student record |
| 🧾 **Examinations** | Exam schedules, marks entry, result publishing |
| 📊 **Admin Dashboard** | Live metrics: admissions, fee collection, hostel occupancy, results and more |
| 🔁 **No Duplicate Entry** | Enter student data once, and every module reads from it |

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React (Vite), React Router, Axios, Tailwind CSS |
| Charts | Recharts / Chart.js |
| Backend | Node.js, Express.js |
| Database | MongoDB Atlas, Mongoose |
| Auth | JWT, bcrypt |
| Payments | Razorpay (test mode) |
| Receipts | PDFKit |
| Email | Nodemailer |
| Deployment | Vercel / Netlify (client), Render (server) |

---

## 📁 Project Structure

```
CampusSync/
├── client/                      # React frontend
│   └── src/
│       ├── components/          # Reusable UI components
│       ├── pages/               # Dashboard, Admissions, Fees, Hostel, Exams, Library
│       ├── context/             # Auth context
│       ├── services/            # API calls (Axios)
│       └── App.jsx
├── server/                      # Express backend
│   ├── config/                  # DB connection, env
│   ├── controllers/
│   ├── middleware/              # auth, role check, error handler
│   ├── models/                  # Student, Admission, Fee, Hostel, Exam, Library
│   ├── routes/
│   ├── utils/                   # receipt generator, mailer
│   └── server.js
├── .env.example
├── .gitignore
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js v18+
- MongoDB Atlas account (or local MongoDB)
- Git

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/CampusSync.git
cd CampusSync

# 2. Setup the server
cd server
npm install
cp ../.env.example .env      # fill in your values
npm run dev

# 3. Setup the client (new terminal)
cd client
npm install
npm run dev
```

### Environment Variables

```env
PORT=5000
MONGO_URI=your_mongodb_atlas_uri
JWT_SECRET=your_secret_key
JWT_EXPIRES_IN=7d
RAZORPAY_KEY_ID=your_key_id
RAZORPAY_KEY_SECRET=your_key_secret
EMAIL_USER=your_email
EMAIL_PASS=your_app_password
CLIENT_URL=http://localhost:5173
```

---

## 👥 Team & Work Division

**Team size:** 6 members. Each person owns one area end to end (backend + frontend for that module), while two people own shared foundations.

| # | Member | Role | Owns |
|---|---|---|---|
| 1 | _Name 1_ | 🧭 **Team Lead & Backend Architect** | Project setup, MongoDB schema design, `Student` core model, JWT auth, RBAC middleware, API standards, code reviews, merging PRs |
| 2 | _Name 2_ | 🎨 **Frontend Lead & UI/UX** | Design system, layout/navigation, routing, login & role-based UI, **admin dashboard** and charts |
| 3 | _Name 3_ | 📝 **Admissions Module** | Application form, document upload, verification/approval workflow, student record creation on approval |
| 4 | _Name 4_ | 💰 **Fees & Payments Module** | Fee structure, Razorpay integration, payment history, dues, **PDF receipt generation**, email receipts |
| 5 | _Name 5_ | 🏠 **Hostel & Library Modules** | Room allocation, vacancy tracking, book issue/return, fines, linking both to the student record |
| 6 | _Name 6_ | 🧾 **Exams, QA & DevOps** | Exam schedule, marks entry, results, API testing (Postman), deployment, CI, documentation, demo video and PPT |

### Shared responsibilities
- **Everyone:** write APIs with consistent response format, handle errors, add validation, and create a PR for every feature.
- **Members 1 & 2:** unblock others early. Auth and layout must be ready in the first phase.
- **Member 6:** keeps the deployed demo working and prepares the final presentation material.

### 🗓️ Suggested Timeline

| Phase | Focus | Who |
|---|---|---|
| **Phase 1** | Repo setup, schemas, auth, RBAC, layout, routing | 1, 2 (others set up env and study the schemas) |
| **Phase 2** | Module development (admissions, fees, hostel, library, exams) | 3, 4, 5, 6 |
| **Phase 3** | Dashboard integration, receipt/email flows, cross-module linking | 1, 2, 4 |
| **Phase 4** | Testing, bug fixing, deployment, documentation | All, led by 6 |
| **Phase 5** | Demo video, PPT, final polish, rehearsal | All |

---

## 🌿 Git Workflow

```
main        → stable, demo-ready code only
develop     → integration branch
feature/*   → one branch per feature (e.g. feature/fee-receipts)
```

1. Create a branch from `develop`: `git checkout -b feature/<name>`
2. Commit often with clear messages (`feat:`, `fix:`, `docs:`, `refactor:`)
3. Open a Pull Request into `develop`
4. At least **one teammate reviews** before merging
5. Team Lead merges `develop` into `main` for milestones

---

## 🗺️ Roadmap

- [ ] Project setup and database schemas
- [ ] Authentication and role-based access
- [ ] Admissions module
- [ ] Fee module with payment and PDF receipts
- [ ] Hostel allocation module
- [ ] Library module
- [ ] Examination module
- [ ] Admin dashboard with live metrics
- [ ] Email notifications
- [ ] Testing and deployment
- [ ] Demo video and presentation

**Future scope:** SMS/WhatsApp alerts, attendance module, parent portal, multi-institution support, multilingual UI (English/Hindi).

---

## 📸 Screenshots

_Add screenshots of the dashboard, fee receipt, and admission flow here once ready._

---

## 🤝 Contributing

1. Fork the repo
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m "feat: add amazing feature"`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

<div align="center">

**Built with ❤️ for Smart India Hackathon 2025**

⭐ Star this repo if you find it useful!

</div>
