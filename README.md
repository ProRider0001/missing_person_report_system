# missing_person_report_system
The Missing Person Management System is a centralized web platform that streamlines reporting and managing missing person cases. It provides secure storage, easy search, and quick updates to improve teamwork and speed up responses.


Missing Person System (MPS)

A full-stack web application for reporting and enquiring about missing persons, built with **Next.js**, **React**, **Node.js**, and **PostgreSQL**.

---
📁 Project Structure
```
missing-person-system/
mps3/
├── .env.example
├── package.json
├── database/
│   └── schema.sql
├── lib/
│   ├── db.js
│   └── auth.js
├── pages/
│   ├── _app.js
│   ├── index.js
│   ├── dashboard.js
│   ├── report.js
│   ├── enquiry.js
│   ├── police.js
│   └── api/
│       ├── auth/
│       │   ├── login.js
│       │   └── register.js
│       ├── cases/
│       │   ├── report.js
│       │   └── police-dashboard.js
│       └── enquiries/
│           └── submit.js
└── styles/
    └── globals.css
```

---

## 🚀 Setup Instructions

### 1. Prerequisites

- **Node.js** v18+
- **PostgreSQL** v14+
- **npm** or **yarn**

---

### 2. Clone and Install

```bash
git clone <your-repo-url>
cd missing-person-system
npm install
```

---

### 3. PostgreSQL Database Setup

```bash
# Create the database
psql -U postgres
CREATE DATABASE missing_person_db;
\q

# Run the schema
psql -U postgres -d missing_person_db -f database/schema.sql
```

---

### 4. Environment Variables

```bash
cp .env.example .env.local
```

Edit `.env.local`:

```env
DB_HOST=localhost
DB_PORT=5432
DB_NAME=missing_person_db
DB_USER=postgres
DB_PASSWORD=your_password_here
JWT_SECRET=your-very-long-random-secret-key-here
```

---

### 5. Run the Application

```bash
# Development
npm run dev

# Production build
npm run build
npm start
```

Open [http://localhost:3000](http://localhost:3000)

---

