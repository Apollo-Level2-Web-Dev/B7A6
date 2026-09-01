# 🚀 B7A6 Backend Project Assignment

> 💡 **Note:** This is a **backend-focused** assignment. You will build a robust, scalable, and secure RESTful API. No frontend UI is required; all functionality must be demonstrated via API testing tools like Postman or Thunder Client.

---

## 🔍 Find Your Assignment 

> 💡 Check your Student ID by clicking your **profile image** on the [Programming Hero Website](https://web.programming-hero.com/profile).

| Last Digit of Student ID | Assignment |
|:------------------------:|:-----------|
| **1** | **Courier & Logistics Platform** 🚚 |
| **2** | **Blood Donation & Emergency Platform** 🩸 |
| **3** | **Load Shedding & Power Management** ⚡ |
| **4** | **Developer Assessment Platform** 💻 |
| **5** | **Emergency Ambulance Dispatch** 🚑 |
| **6** | **Housing & Roommate Platform** 🏠 |
| **7** | **Field Service Management** 🔧 |
| **8** | **Project Management SaaS** 📋 |
| **9** | **University Management System** 🎓 |
| **0** | **City Complaint & Service Platform** 🏙️ |

> 📚 **Explore the full Idea Hub:** [Project Idea Hub](https://github.com/Apollo-Level2-Web-Dev/B7A6/blob/main/idea-hub.md)

> 💡 **Note:** You may customize the selected project or choose a completely unique project outside this list. However, regular e-commerce clones or projects already covered in this course are **not allowed**. The core problem domain, the 3-role requirement, and the overall project complexity must strictly meet our expectations.

---

## ⚠️ Mandatory Requirements

> [!CAUTION]
> **MANDATORY - READ CAREFULLY**
> 
> The following requirements are **strictly mandatory**. Failure to complete any of these may result in significant mark deductions or **0 marks** for the affected section:
> 
> 1. **API Documentation**: Share a complete Postman Collection or Swagger/OpenAPI documentation covering all important endpoints.
> 2. **Consistent API Responses**: All APIs must return a structured JSON response:
>    - **Success**: `{ "success": true, "message": "Operation successful", "data": {} }`
>    - **Error**: `{ "success": false, "message": "Something went wrong", "errors": [] }`
> 3. **Commits**: Minimum **20 meaningful** backend commits with descriptive messages (e.g., `feat:`, `fix:`, `docs:`).
> 4. **Input Validation**: Server-side validation (Zod/Joi) is required on all applicable endpoints with proper error messages.
> 5. **Authentication & Authorization**: Implement authentication (Email/Password + GCP Social Login) and strict role-based authorization for **3 distinct roles**.
> 6. **Admin Credentials**: Provide working demo admin email and password for evaluation.
> 7. **Payment Integration**: Must integrate **bKash, Stripe, or SSLCommerz** for real payment processing. Simulated/fake payments are **NOT** accepted.
> 8. **Database**: Use **PostgreSQL with Prisma**, implementing proper relationships, constraints, indexing, and transactions.
> 9. **Deployment**: Provide a working live API URL (e.g., Vercel Serverless Functions or Render).
> 10. **Video Explanation**: Submit a 5–10 minute API walkthrough video.

---

## 📊 Marks Distribution

| # | Category | Weight | Details |
|:-:|:---------|:------:|:--------|
| 1 | API Design & Documentation | 15% | RESTful design, endpoint structure, Postman/Swagger docs |
| 2 | Database Design & Schema | 15% | Prisma schema, relationships, constraints, migrations, seed data |
| 3 | Authentication & Authorization | 15% | Auth (Email + GCP), 3 roles, JWT/session handling, protected routes |
| 4 | Core Functionality & Business Logic | 20% | CRUD, workflows, status management, role-based operations |
| 5 | Error Handling & Validation | 10% | Input validation, structured errors, 404 handling, edge cases |
| 6 | Payment Integration | 10% | bKash/Stripe/SSLCommerz integration, payment flow, status tracking |
| 7 | Performance & Code Quality | 5% | Indexing, Redis caching, modular architecture, clean code |
| 8 | Deployment | 5% | Working production API, environment configuration, DB connection |
| 9 | Commit History | 2% | 20 meaningful backend commits |
| 10 | Video Explanation | 3% | 5–10 minute API walkthrough |
| **Total** | | **100%** | |

---

## 📋 Project Requirements

> ⏱️ **Detailed Guidelines:** Please read the complete project requirements, tech stack, and API rules here:  
> 👉 [Project Requirements & API Guidelines](https://github.com/Apollo-Level2-Web-Dev/B7A6/blob/main/project_requirements.md)

---

## 📅 Timeline: 5-Day Work Breakdown

> ⏱️ **Recommended Schedule:** Maintain steady progress to avoid last-minute stress and ensure a clean Git history.  
> 👉 [View the 5-Day Work Breakdown](https://github.com/Apollo-Level2-Web-Dev/B7A6/blob/main/timeline-breakdown.md)

---

## 🗓️ Submission Deadlines

| Deadline | Maximum Marks |
|:---------|:-------------:|
| **September 07, 2026, 11:59 PM** | 60 Marks |
| **September 08, 2026, 11:59 PM** | 50 Marks |
| **September 09, 2026 – September 23, 2026, 11:59 PM** | 30 Marks |

---

## 📦 What to Submit

Please format your submission exactly like this example:

```text
Project Name    : Courier & Logistics Platform
Backend Repo    : https://github.com/your-username/courier-backend
Live API        : https://courier-api.vercel.app
API Docs        : https://documenter.getpostman.com/view/xyz
Demo Video      : https://drive.google.com/file/d/xyz/view
Admin Email     : admin@courier.com
Admin Password  : ********
```

> ⚠️ **Security Warning:** Never submit personal passwords or production secrets. Create dedicated, secure demo credentials specifically for evaluation.

---

## 🎥 Video Explanation Guide

**Duration:** 5–10 minutes  
**Language:** English or Bengali  

**What to Cover:**
1. **Project Overview & Architecture**: Briefly explain the project name, the problem it solves, and your backend architecture (Routes → Controllers → Services → Prisma).
2. **Demonstrate All 3 Roles**: Use **Postman / Thunder Client** to demonstrate actual API requests for all three roles. Show that a role *cannot* access endpoints belonging to another role (e.g., returning a `403 Forbidden`).
3. **Demonstrate CRUD**: Show meaningful CRUD operations via API requests (POST, GET, PATCH/PUT, DELETE) with clear request bodies and responses.
4. **Demonstrate Validation & Error Handling**: Intentionally trigger a validation error (e.g., invalid email format) and show the structured error response. Show a `404 Not Found` or `401 Unauthorized` example.
5. **Demonstrate Payment Flow**: Walk through the payment API flow: Create Payment Session → Redirect/Response → Success/Cancel handling → Backend verification → Payment status update in the database.
6. **Explain One Technical Challenge**: Briefly explain one meaningful problem you solved (e.g., Complex Prisma transactions, GCP Social Login integration, Redis caching strategy, or payment webhook handling).

**Recording Options:**
- **Loom**: Record and share the link directly.
- **OBS**: Record and upload to Google Drive (ensure sharing is set to "Anyone with the link" → Viewer).

---

> 🚀 **Final Goal:** Build a backend that is more than just a collection of endpoints. Your project should demonstrate a clear, logical path from **Problem → Requirements → Database Design → API Design → Auth → Business Logic → Validation → Payment → Testing → Deployment**. Build a rock-solid backend you can explain, defend, and be proud of!
