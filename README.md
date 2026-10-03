# Examination System API

A backend Examination System built with **ASP.NET Core / .NET 10**, designed to manage the complete examination lifecycle for administrators and students.

The project was developed as a **team project during an Advanced .NET Backend Bootcamp**, following modern backend development practices and a feature-oriented architecture.

---

## 📌 Overview

The Examination System provides APIs for managing users, diplomas, quizzes, questions, student enrollments, exam attempts, answers, results, and analytics.

The system is designed around business capabilities rather than traditional technical layers, using **Vertical Slice Architecture** with **CQRS and MediatR**.

---

## ✨ Main Features

### 🔐 Identity & Authentication

- User registration
- Email verification
- Login
- Refresh tokens
- Logout
- Forgot password
- Password reset
- Role-based access
- Student and Admin accounts

---

### 🎓 Diploma Management

- Browse available diplomas
- View diploma details
- Student enrollment
- Student dashboard
- Admin diploma management

---

### 📝 Quiz Management

Administrators can manage the quiz lifecycle including:

- Quiz creation
- Quiz update
- Quiz deletion
- Question management
- Question options management
- Question ordering
- Quiz publish-readiness validation
- Quiz publishing
- Quiz unpublishing

Quiz configuration includes information such as:

- Duration
- Pass score
- Maximum attempts
- Questions
- Answer options

---

### 👨‍🎓 Student Attempts

Students can interact with quizzes through timed attempts:

- Start an attempt
- Check remaining time
- Submit answers
- Submit an attempt
- Enforce attempt deadlines
- Track attempt status
- View attempt history
- View attempt results

The system uses a server-side deadline for timed attempts.

---

### 📊 Results & Analytics

The system provides functionality for:

- Attempt results
- Student attempt history
- Attempt monitoring
- Attempt details
- Performance analytics
- Admin dashboard information
- Searching and reviewing attempts

---

## 🏗️ Architecture

The project follows **Vertical Slice Architecture (VSA)**.

Instead of organizing the application primarily by technical layers, functionality is grouped by business capability.

### Feature Structure

```text
Features/
└── Module/
    └── Feature/
        ├── Commands/
        ├── Queries/
        ├── Handlers/
        ├── Controllers/
        ├── Validators/
        ├── Orchestrators/
        └── Response / DTOs


## ⚙️ Engineering Patterns

The project applies several backend design patterns and practices:

- **CQRS** — Separating read and write operations into dedicated Queries and Commands.
- **MediatR** — Decoupling requests from their handlers and simplifying application communication.
- **Orchestrator Pattern** — Coordinating multiple Commands and Queries within complex business workflows.
- **Unit of Work** — Managing database persistence and transaction boundaries across business operations.
- **SavePoints** — Supporting partial rollback within transactions when workflows contain optional operations.

These patterns help keep the business logic focused, maintainable, and easier to extend.
