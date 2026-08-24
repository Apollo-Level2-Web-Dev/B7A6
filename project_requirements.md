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
- **Security**: Hash passwords securely, never expose secrets, protect all private routes, and secure payment verification.
- **Performance**: Optimize your backend by using database indexing, efficient Prisma queries (e.g., using `select` to avoid over-fetching), and Redis caching where beneficial.

---

## ⚙️ Minimum 20 APIs Requirement

Each project must implement and document **at least 20 meaningful API endpoints**. 

These APIs must represent the actual functionality of your selected project. You should not create unnecessary, duplicate, or dummy endpoints just to fulfill the API count.

### API Technical Requirements

- **Consistent Response Format**: You must use a standardized JSON structure for all endpoints:
  - **Success**: `{ "success": true, "message": "Operation successful", "data": {} }`
  - **Error**: `{ "success": false, "message": "Something went wrong", "errors": [] }`
- **Authentication & Authorization**: Protected APIs must use **Bearer Token authentication**. You must implement strict **role-based middleware** to enforce the 3 project roles.
- **Validation & Error Handling**: All applicable APIs must have proper **server-side validation** (using Zod or Joi) and return structured error messages for invalid inputs.
- **Advanced Data Fetching**: 
  - At least one list API must support **pagination** (e.g., `?page=1&limit=10`).
  - At least one list API must support **filtering and/or sorting** (e.g., `?status=active&sortBy=createdAt`).
  - Implement **search functionality** where relevant to the project domain.
- **Business Logic**: Implement meaningful **business operations beyond basic CRUD** (e.g., status transitions, resource assignments, complex calculations).
- **RESTful Design & Documentation**: Follow proper RESTful naming conventions. All APIs must be connected to the actual database and properly documented using **Postman or Swagger/OpenAPI**.

### Minimum API Coverage

Your 20+ APIs should cover most of the following areas:

| Category | Requirement |
|---|---|
| **Authentication** | Register, login, token management (refresh/logout) |
| **User/Profile** | Profile management and user-related operations |
| **Core Resources** | Create, read, update, delete (CRUD) |
| **Business Operations** | Project-specific workflows, actions, and state changes |
| **Search & Filtering** | Search, filtering, sorting, and pagination |
| **Payment** | Payment initiation, verification/webhook, and status tracking |
| **Admin** | User management, statistics, or project-specific administration |

### Example API Structure

A complete project will contain APIs structured similar to this:

```http
# Authentication
POST   /api/auth/register
POST   /api/auth/login
POST   /api/auth/refresh-token

# User / Profile
GET    /api/users/me
PATCH  /api/users/me

# Core Resources (with Pagination & Filtering)
POST   /api/resources
GET    /api/resources                 # Supports ?page=1&limit=10&status=active
GET    /api/resources/:id
PATCH  /api/resources/:id
DELETE /api/resources/:id
GET    /api/resources/search?q=keyword

# Business Operations
POST   /api/resources/:id/assign
PATCH  /api/resources/:id/status
POST   /api/resources/:id/cancel
GET    /api/resources/my-assigned

# Payment Integration
POST   /api/payments/initiate
POST   /api/payments/webhook
GET    /api/payments/:id

# Admin Operations
GET    /api/admin/users
PATCH  /api/admin/users/:id/role
GET    /api/admin/dashboard-stats
