# hcl-hackathon
# Healthcare Wellness Portal

A full-stack healthcare web application that helps **patients track wellness goals and reminders** while allowing **healthcare providers to monitor patient engagement and compliance**.

The system is built using the **MERN Stack (MongoDB, Express, React, Node.js)** and demonstrates secure authentication, role-based access control, and RESTful API architecture.

---

# Project Overview

The Healthcare Wellness Portal is designed to support preventive healthcare by enabling patients to monitor daily wellness activities such as:

- Daily step count
- Water intake
- Sleep hours

The system also allows patients to set **preventive health reminders** for checkups, medications, and wellness activities.

Healthcare providers can monitor assigned patients through a **provider dashboard** that shows patient progress and goal compliance.

---

# Key Features

## Patient Features

- User registration and login
- Secure authentication using JWT
- Wellness goal tracking
- Daily progress monitoring
- Health reminders management
- Medical profile management

Examples of tracked wellness goals:

- Steps per day
- Water intake
- Sleep hours

---

## Provider Features

Healthcare providers can:

- View assigned patients
- Monitor weekly goal completion
- Track patient engagement

Provider dashboard shows:

- Patient name
- Weekly goal completion
- Compliance status

---

# Tech Stack

## Frontend
- React
- React Router
- Axios
- Tailwind CSS

## Backend
- Node.js
- Express.js

## Database
- MongoDB
- Mongoose ODM

## Security
- JWT Authentication
- bcrypt password hashing
- Role-based access control

---

# System Architecture
React Frontend
│
▼
HTTP Requests (REST API)
│
▼
Node.js + Express Backend
│
▼
Database Queries
│
▼
MongoDB Database

The frontend communicates with backend APIs which interact with MongoDB to store and retrieve patient data.

---

# Project Structure
healthcare-portal
│
├── backend
│ ├── models
│ │ ├── User.js
│ │ ├── PatientProfile.js
│ │ ├── WellnessGoal.js
│ │ └── Reminder.js
│ │
│ ├── routes
│ │ ├── authRoutes.js
│ │ ├── patientRoutes.js
│ │ ├── providerRoutes.js
│ │ └── publicRoutes.js
│ │
│ ├── middleware
│ │ └── authMiddleware.js
│ │
│ ├── controllers
│ │
│ ├── server.js
│ └── .env
│
├── frontend
│ ├── src
│ │ ├── components
│ │ ├── pages
│ │ ├── services
│ │ ├── context
│ │ ├── App.jsx
│ │ └── main.jsx
│
└── README.md


---

# API Endpoints

## Authentication APIs

| Method | Endpoint | Description |
|------|------|------|
| POST | /api/auth/register | Register new user |
| POST | /api/auth/login | Login user |
| GET | /api/auth/me | Get logged-in user |

---

## Patient APIs

| Method | Endpoint | Description |
|------|------|------|
| GET | /api/patient/profile | Get patient profile |
| PUT | /api/patient/profile | Update patient profile |
| GET | /api/patient/goals | List wellness goals |
| POST | /api/patient/goals | Create or update goal |
| GET | /api/patient/reminders | List reminders |
| POST | /api/patient/reminders | Create reminder |
| PUT | /api/patient/reminders/:id | Update reminder |

---

## Provider APIs

| Method | Endpoint | Description |
|------|------|------|
| GET | /api/provider/patients | View assigned patients |

---

# Installation Guide

## Clone Repository
git clone https://github.com/your-username/healthcare-wellness-portal.git

cd healthcare-wellness-portal

---

# Backend Setup

Navigate to backend folder:
cd backend


Install dependencies:
npm install

Create `.env` file:

MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
PORT=5000

Start backend server:

npm run dev

Backend runs on:

http://localhost:5000

---

# Frontend Setup

Navigate to frontend folder:

cd frontend

Install dependencies:

npm install

Start development server:

npm run dev

Frontend runs on:

http://localhost:5173


---

# Security Considerations

The system implements several security practices:

- Password hashing using bcrypt
- JWT based authentication
- Token-protected routes
- Role-based authorization (patient / provider)
- Sensitive configuration stored in environment variables

---

# Future Improvements

Potential enhancements include:

- Mobile application support
- Integration with wearable devices
- Advanced health analytics
- Appointment scheduling
- Notification and alert system
- AI-based health insights

---

# Contributors

Project developed as part of a hackathon.

Contributors may include team members responsible for:

- Frontend development
- Backend API development
- Database design
- System architecture

---

# License

This project is intended for educational and hackathon purposes.
