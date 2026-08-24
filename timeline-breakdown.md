## 📅 Recommended 5-Day Timeline

> ⏱️ **Recommended Workload:** 5–8 hours per day. 
> 
> **Pro Tip:** Consistency is key. Spread your work across all five days to avoid burnout, ensure deep understanding, and maintain a clean Git history. Do not leave everything for the final day!

### 🗓️ High-Level Overview

| Day | Focus Area | Expected Output |
|:---:|:---|:---|
| **1** | **Planning & Database** | Requirements, ERD, Prisma schema, project setup, and API planning. |
| **2** | **Auth & Core APIs** | JWT/Bearer Auth, RBAC middleware, user management, and foundational CRUD. |
| **3** | **Business Logic & Validation** | Complete 20+ APIs, Zod validation, error handling, pagination, and transactions. |
| **4** | **Payment & Testing** | Payment gateway integration, webhooks, rigorous testing, and Postman docs. |
| **5** | **Deployment & Submission** | Production deployment, final QA, README polish, video recording, and submission. |

---

### 🟢 Day 1 — Planning, Architecture & Database

**Focus:** Laying a rock-solid foundation. A good schema prevents headaches later.

- [ ] Select project & define the core problem domain.
- [ ] Define the **3 distinct roles** and map out their exact permissions.
- [ ] Plan your **20+ API endpoints** (draft them on paper or a tool like Excalidraw).
- [ ] Identify core entities, relationships, and design the **ERD**.
- [ ] Initialize Node.js, TypeScript, and Express.js project structure.
- [ ] Configure PostgreSQL connection and set up **Prisma ORM**.
- [ ] Create the initial Prisma schema, run migrations, and write seed data.
- [ ] Initialize the Git repository and make your first meaningful commit.
- [ ] **Set up initial deployment (Vercel/Render) and testing workflows** so you can deploy and test your code every single day moving forward.

### 🔵 Day 2 — Authentication & Core APIs

**Focus:** Securing the app and building the basic data flow.

- [ ] Implement User Registration and Login.
- [ ] Implement secure password hashing (e.g., bcrypt).
- [ ] Generate and manage **Bearer Tokens** (JWT).
- [ ] Create Authentication and **Role-Based Authorization (RBAC)** middleware.
- [ ] Build User/Profile management APIs (Get me, Update me).
- [ ] Implement core **CRUD APIs** for your main resource.
- [ ] Create the initial Postman collection and test basic flows.

### 🟡 Day 3 — Business Logic, Validation & Advanced Features

**Focus:** This is the heavy lifting day. Turning basic CRUD into a real application.

- [ ] Complete the remaining APIs to reach the **minimum 20 endpoints**.
- [ ] Implement project-specific business workflows (e.g., status transitions, assignments).
- [ ] Add strict server-side validation using **Zod or Joi** on all POST/PATCH/PUT routes.
- [ ] Implement a **centralized error handling** middleware with structured JSON responses.
- [ ] Add **pagination, filtering, and sorting** to your `GET` list endpoints.
- [ ] Implement database **transactions** for complex operations (e.g., creating an order + updating inventory).
- [ ] Add database **indexes** for frequently queried fields.
- [ ] Integrate Redis (for caching/rate-limiting) or file uploads (Multer/Cloudinary) if applicable.

### 🟠 Day 4 — Payment Integration & Rigorous Testing

**Focus:** Handling money securely and ensuring nothing breaks.

- [ ] Integrate real payment gateway (**Stripe, SSLCommerz, or bKash**).
- [ ] Build payment initiation endpoint (creating session/intent).
- [ ] Implement secure **webhook/callback handling** to verify payments.
- [ ] Build endpoints to track and retrieve payment status.
- [ ] **Test all APIs:** Verify all 3 roles, test validation errors, and check unauthorized requests.
- [ ] Test edge cases (e.g., duplicate entries, not-found resources).
- [ ] Finalize and polish the **Postman/Swagger documentation** with examples.
- [ ] Fix any bugs discovered during testing.

### 🔴 Day 5 — Deployment, Final Polish & Submission

**Focus:** Going live and packaging your project for the evaluators.

- [ ] Configure production environment variables securely.
- [ ] Deploy the backend API (Vercel Serverless / Render) and connect the production PostgreSQL database.
- [ ] Verify all live APIs, authentication flows, role restrictions, and payment integrations.
- [ ] Review Git history to ensure you have **20+ meaningful commits**.
- [ ] Finalize the `README.md` with all submission links and instructions.
- [ ] Prepare dedicated **Admin demo credentials**.
- [ ] Record and upload your **3–5 minute API walkthrough video**.
- [ ] Submit all required links in the assignment portal.

---

### 🎯 Daily Commitment & Testing Rule

> [!IMPORTANT]
> **Do not code for 40 hours on the last day.** 
> 
> You must make meaningful Git commits and **test your deployment every single day** after you finish coding. A steady, daily progression proves you built it yourself, helps you catch integration bugs early, and ensures your live URL is always working and ready for evaluators.
