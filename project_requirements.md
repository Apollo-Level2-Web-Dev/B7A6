## 📋 Project Requirements

> 💡 **Note:** Read these carefully. While not every single point is strictly fixed, you must follow this general guideline to ensure your project meets expectations.

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

> **Note:** You do not need to use every technology in every project. Choose technologies based on the actual requirements of your specific project.

--- 

## 🎯 Core Project Rules

- **Roles**: Each project must have **3 fixed primary roles** (e.g., Customer, Provider, Admin). Role permissions must be strictly defined and enforced.
- **Payment Integration**: This is **MANDATORY**. You must integrate **bKash, Stripe, or SSLCommerz**. Your system must securely handle payment creation, success/cancellation callbacks, and status tracking. *Cash on Delivery, Pay Later, or fake manual status updates are NOT accepted.*
- **No Frontend Required**: This is a backend-focused assignment. You do not need to build a UI. Use Postman, Thunder Client, or Swagger to demonstrate your API.
- **Security & Protection**: 
  - Hash passwords securely, never expose secrets, and protect all private routes.
  - Implement **Rate Limiting** (e.g., using `express-rate-limit`) to prevent API abuse.
  - Use security headers (e.g., `helmet`) and configure **CORS** properly.
- **Performance & Concurrency**: Optimize your backend using database indexing, efficient Prisma queries (e.g., using `select`), and Redis caching. Use **database transactions** to handle concurrency and prevent race conditions (e.g., double-booking a resource).

---

## ⚙️ Minimum 20 APIs Requirement

Each project must implement and document **at least 20 meaningful API endpoints**. 

These APIs must represent the actual functionality of your selected project. You should not create unnecessary, duplicate, or dummy endpoints just to fulfill the API count.

### API Technical Requirements

- **API Versioning**: Use versioned routes (e.g., `/api/v1/...`) to follow modern RESTful standards.
- **Consistent Response Format**: You must use a standardized JSON structure for all endpoints:
  - **Success**: `{ "success": true, "message": "Operation successful", "data": {} }`
  - **Error**: `{ "success": false, "message": "Something went wrong", "errors": [] }`
- **Authentication & Authorization**: Protected APIs must use **Bearer Token authentication**. You must implement strict **role-based middleware** to enforce the 3 project roles.
- **Validation & Error Handling**: All applicable APIs must have proper **server-side validation** (using Zod or Joi) and return structured error messages for invalid inputs.
- **Advanced Data Fetching**: 
  - At least one list API must support **pagination** (e.g., `?page=1&limit=10`).
  - At least one list API must support **filtering and/or sorting** (e.g., `?status=active&sortBy=createdAt`).
  - Implement **search functionality** where relevant to the project domain.
- **Modern Data Practices**: 
  - Implement **Soft Deletes** (e.g., using a `deletedAt` timestamp) instead of hard deleting records.
  - Implement **Audit Logs / Activity Tracking** for critical actions (e.g., tracking who changed a status or updated a role).
- **Business Logic**: Implement meaningful **business operations beyond basic CRUD** (e.g., status transitions, resource assignments, complex calculations).
- **RESTful Design & Documentation**: Follow proper RESTful naming conventions. All APIs must be connected to the actual database and properly documented using **Postman or Swagger/OpenAPI**.

### Minimum API Coverage

Your 20+ APIs should cover most of the following areas:

| Category | Requirement |
|---|---|
| **Authentication** | Register, login, token management (refresh/logout) |
| **User/Profile** | Profile management and user-related operations |
| **Core Resources** | Create, read, update, soft-delete |
| **Business Operations** | Project-specific workflows, actions, and state changes |
| **Search & Filtering** | Search, filtering, sorting, and pagination |
| **Payment** | Payment initiation, verification/webhook, and status tracking |
| **Admin** | User management, statistics, audit logs, or project-specific administration |

### Example API Structure

A complete project will contain APIs structured similar to this:

```http
# Authentication
POST   /api/v1/auth/register
POST   /api/v1/auth/login
POST   /api/v1/auth/refresh-token

# User / Profile
GET    /api/v1/users/me
PATCH  /api/v1/users/me

# Core Resources (with Pagination & Filtering)
POST   /api/v1/resources
GET    /api/v1/resources                 # Supports ?page=1&limit=10&status=active
GET    /api/v1/resources/:id
PATCH  /api/v1/resources/:id
DELETE /api/v1/resources/:id             # Soft delete
GET    /api/v1/resources/search?q=keyword

# Business Operations
POST   /api/v1/resources/:id/assign
PATCH  /api/v1/resources/:id/status
POST   /api/v1/resources/:id/cancel
GET    /api/v1/resources/my-assigned

# Payment Integration
POST   /api/v1/payments/initiate
POST   /api/v1/payments/webhook
GET    /api/v1/payments/:id

# Admin Operations
GET    /api/v1/admin/users
PATCH  /api/v1/admin/users/:id/role
GET    /api/v1/admin/dashboard-stats
GET    /api/v1/admin/audit-logs          # Track system changes
