# 🚀 B7A6 Backend Project Assignment

> 💡 **Note:** This is a **backend-focused** assignment. You will build a robust, scalable, and secure RESTful API. No frontend UI is required; all functionality must be demonstrated via API testing tools like Postman or Thunder Client.

---

## 🔍 Find Your Assignment 

> Check your Student ID by clicking your **profile image** on the [Programming Hero Website](https://web.programming-hero.com/profile).

| Last Digit of Student ID | Assignment |
|:------------------------:|------------|
| **1** | **Courier & Logistics Platform** 🚚 |
| **2** | **Blood Donation & Emergency Platform** 🩸 |
| **3** | **Load Shedding & Power Management** ⚡  |
| **4** | **Developer Assessment Platform** 💻  |
| **5** | **Emergency Ambulance Dispatch** 🚑 |
| **6** | **Housing & Roommate Platform** 🏠 |
| **7** | **Field Service Management** 🔧 |
| **8** | **Project Management SaaS** 📋 |
| **9** | **University Management System** 🎓 |
| **0** | **City Complaint & Service Platform** 🏙️ |


> Pick from here [PROJECT_IDEAS](https://github.com/Apollo-Level2-Web-Dev/B7A6/blob/main/PROJECT_IDEAS.md)

> 💡 **Note:** You may customize the selected project or choose a completely unique project outside this list. However, regular e-commerce clones or projects already covered in this course are **not allowed**. The core problem domain, the 3-role requirement, and the overall project complexity must strictly meet our expectations.

---

## ⚠️ Mandatory Requirements

> [!CAUTION]
> **MANDATORY - READ CAREFULLY**
> 
> The following requirements are **strictly mandatory**. Failure to complete any of these may result in significant mark deductions or **0 marks** for the affected section:
> 1. **API Documentation**: Share Postman Collection or Swagger/OpenAPI documentation covering all important endpoints.
> 2. **Consistent API Responses**: All API must return a structured JSON response:
  Success: `{ "success": true, "message": "Operation successful", "data": {} }`
  Error: `{ "success": false, "message": "Something went wrong", "errors": [] }`.
> 3. **Commits**: Minimum **20 meaningful** backend commits with descriptive messages (e.g., `feat:`, `fix:`, `docs:`).
> 4. **Input Validation**: Server-side validation (Zod/Joi) is required on all applicable endpoints with proper error messages.
> 5. **Authentication & Authorization**: Implement authentication (Email/Password + GCP Social Login) and strict role-based authorization for **3 distinct roles**.
> 6. **Admin Credentials**: Provide working demo admin email and password for evaluation.
> 7. **Payment Integration**: Must integrate **bKash, Stripe, or SSLCommerz** for real payment processing. Simulated/fake payments are **NOT** accepted.
> 8. **Database**: Use **PostgreSQL with Prisma**, implementing proper relationships, constraints, indexing, and transactions.
> 9. **Deployment**: Provide a working live API URL (e.g., Vercel Serverless Functions or Render).
> 10. **Video Explanation**: Submit a 5-10 minute API walkthrough video.

---

## 📊 Marks Distribution

| # | Category | Weight | Details |
|:-:|----------|:------:|---------|
| 1 | API Design & Documentation | 15% | RESTful design, endpoint structure, Postman/Swagger docs |
| 2 | Database Design & Schema | 15% | Prisma schema, relationships, constraints, migrations, seed data |
| 3 | Authentication & Authorization | 15% | Auth (Email + GCP), 3 roles, JWT/session handling, protected routes |
| 4 | Core Functionality & Business Logic | 20% | CRUD, workflows, status management, role-based operations |
| 5 | Error Handling & Validation | 10% | Input validation, structured errors, 404 handling, edge cases |
| 6 | Payment Integration | 10% | bKash/Stripe/SSLCommerz integration, payment flow, status tracking |
| 7 | Performance & Code Quality | 5% | Indexing, Redis caching, modular architecture, clean code |
| 8 | Deployment | 5% | Working production API, environment configuration, DB connection |
| 9 | Commit History | 2% | 20 meaningful backend commits |
| 10 | Video Explanation | 3% | 5-10 minute API walkthrough |
| **Total** | | **100%** | |

---

## 📅 Timeline: 5-Day Work Breakdown

> ⏱️ **Recommendation:** Maintain steady progress throughout all five days instead of completing everything at the last moment.

| Day | Focus | Expected Output |
|:---:|-------|-----------------|
| **Day 1** | Planning & Database | Project idea, roles, ERD, Prisma schema, Node/TS setup, Git init, Deployment init |
| **Day 2** | Authentication & Core APIs | Email/GCP Auth, role middleware, user/profile APIs, main CRUD endpoints |
| **Day 3** | Business Logic & Validation | Workflows, DB transactions, Zod/Joi validation, centralized error handling, Redis |
| **Day 4** | Payment, Testing & Docs | bKash/Stripe/SSLCommerz integration, API testing, Postman docs, bug fixing |
| **Day 5** | Deployment & Presentation | Production deployment, final verification, README update, demo video recording |


---

## 📅 Timeline

| Deadline | Maximum Marks |
|----------|:-------------:|
| **September 05, 2026, 11:59 PM** | 60 Marks |
| SeptemberSep 06, 2026, 11:59 PM** | 50 Marks |
| **From September 7, 2026 To September 7, 2026, 11:59 PM** | 30 Marks |
---

## 📦 What to Submit

```text
Project Name    : XYZ Platform
Backend Repo    : https://github.com/your-username/xyz-backend
Live API        : https://xyz-api.vercel.app
API Docs        : https://documenter.getpostman.com/view/xyz
Demo Video      : https://drive.google.com/file/d/xyz/view
Admin Email     : admin@xyz.com
Admin Password  : ********
```
> ⚠️ **Never submit personal passwords or production secrets.** Create dedicated demo credentials for evaluation.

---

## 🎥 Video Explanation Guide

**Duration:** 5-10 minutes  
**Language:** English or Bengali  

**What to Cover:**
1. **Project Overview & Architecture**: Briefly explain the project name, problem solved, and backend architecture (Routes → Controllers → Services → Prisma).
2. **Demonstrate All 3 Roles**: Use **Postman / Thunder Client** to demonstrate actual API requests for all three roles. Show that a role *cannot* access endpoints belonging to another role (403 Forbidden).
3. **Demonstrate CRUD**: Show meaningful CRUD operations via API requests (POST, GET, PATCH/PUT, DELETE) with request bodies and responses.
4. **Demonstrate Validation & Error Handling**: Trigger a validation error (e.g., invalid email) and show the structured error response. Show a 404 Not Found or Unauthorized example.
5. **Demonstrate Payment Flow**: Show the payment API flow: Create Payment Session → Redirect/Response → Success/Cancel handling → Backend verification → Payment status update in DB.
6. **Explain One Technical Challenge**: Briefly explain one meaningful problem you solved (e.g., Complex Prisma transactions, GCP Social Login integration, Redis caching strategy, or payment webhook handling).

**Recording Options:**
- **Loom**: Record and share the link directly.
- **OBS**: Record and upload to Google Drive (set to "Anyone with the link" → Viewer).

---

## 🛠️ Tech Stack

| Category | Technology | Purpose |
|----------|------------|---------|
| **Runtime & Framework** | Node.js, TypeScript, Express.js | REST API development with type safety |
| **Database & ORM** | PostgreSQL + Prisma | Relational database with relation management, indexing, and transactions |
| **Validation** | Zod / Joi | Strict API-level input validation |
| **Linting & Formatting** | Biome / ESLint / Prettier / oxlint | Code quality, consistency, and formatting |
| **Caching & State (Optional)** | Redis | Caching, temporary state, or rate limiting |
| **Authentication** | Custom / Better Auth / Clerk | Email/Password + Social Login (GCP) |
| **Email (Optional)** | Nodemailer / Resend | Transactional emails and notifications |
| **File Storage** | Multer & Cloudinary | Secure file/image upload and storage |
| **Payments** | bKash / Stripe / SSLCommerz | Real payment processing and status tracking |
| **Documentation** | Postman | API testing and interactive documentation |
| **Deployment** | Vercel (Serverless Functions) / Render | Production backend API deployment |

> **Note:** You do not need to use every technology in every project. Choose technologies based on the actual requirements of your project.

---

## 🎯 Key Rules

- **Roles**: Each project must have **3 fixed primary roles** (e.g., Customer, Provider, Admin). Role permissions must be strictly enforced on the backend via middleware.
- **Payment**: Payment integration is **MANDATORY**. You must integrate **bKash, Stripe, or SSLCommerz**. The system must include endpoints for creating a payment, handling success/cancellation, and tracking payment status securely. *Cash on Delivery or fake manual status updates are NOT accepted.*
- **No Frontend Required**: This is a backend-focused assignment. Use Postman, Thunder Client, or Swagger to demonstrate your API.
- **API Response Format**: Use a consistent response structure.
  - **Success**: `{ "success": true, "message": "Operation successful", "data": {} }`
  - **Error**: `{ "success": false, "message": "Something went wrong", "errors": [] }`
- **Performance**: Consider database indexing, pagination, efficient Prisma queries (e.g., `select`), and Redis caching where beneficial.
- **Security**: Hash passwords securely, never expose secrets, validate all incoming data, protect private routes, and secure payment verification.

---

> 🚀 **Goal:** Build a backend that is more than a collection of endpoints. Your project should demonstrate a clear path from **Problem → Requirements → Database Design → API Design → Auth → Business Logic → Validation → Payment → Testing → Deployment**. Build a rock-solid backend you can explain, defend, and be proud of!
