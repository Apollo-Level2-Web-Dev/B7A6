
# 📋 Project Requirements


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

### ⚙️ Minimum 20 APIs

Each project must implement and document **at least 20 meaningful API endpoints**.

The APIs must represent the actual functionality of the selected project. Students should not create unnecessary or duplicate endpoints only to fulfill the API count.

#### Requirements

- Minimum **20 meaningful APIs** are mandatory.
- All APIs must be properly documented using **Postman or Swagger/OpenAPI**.
- APIs must be connected to the actual database and business logic.
- Implement proper **RESTful API design**.
- Protected APIs must use **Token authentication**.
- Implement **role-based authorization** for the project's 3 roles.
- At least one list API must support **pagination**.
- At least one list API must support **filtering and/or sorting**.
- Implement **search functionality** where it is relevant to the selected project.
- Implement meaningful **business operations beyond basic CRUD**.
- Payment-related APIs must be included as part of the mandatory payment integration.
- Admin-specific APIs must be protected with proper admin authorization.
- All applicable APIs must have proper **server-side validation** and **error handling**.

#### Minimum API Coverage

The 20+ APIs should cover most of the following areas:

| Category | Requirement |
|---|---|
| Authentication | Register, login, token management |
| User/Profile | Profile management and user-related operations |
| Core Resources | Create, read, update, delete |
| Business Operations | Project-specific workflows and actions |
| Search & Filtering | Search, filtering, sorting, pagination |
| Payment | Payment initiation, verification/webhook, status |
| Admin | User management, statistics, or project-specific administration |

> The exact API structure will depend on the selected project. Students are responsible for designing APIs that make sense for their project's requirements.

#### Example

A project may contain APIs such as:

```http
POST   /api/auth/register
POST   /api/auth/login
POST   /api/auth/refresh-token

GET    /api/users/me
PATCH  /api/users/me

POST   /api/resources
GET    /api/resources
GET    /api/resources/:id
PATCH  /api/resources/:id
DELETE /api/resources/:id
GET    /api/resources/search

POST   /api/resources/:id/assign
PATCH  /api/resources/:id/status
POST   /api/resources/:id/cancel
GET    /api/resources/my-assigned

POST   /api/payments/initiate
POST   /api/payments/webhook
GET    /api/payments/:id

GET    /api/admin/users
PATCH  /api/admin/users/:id/role
GET    /api/admin/dashboard-stats
````

> ❌ Endpoints such as `/api/test1`, `/api/test2`, duplicate endpoints, or APIs without meaningful functionality will **not** count toward the 20 API requirement.


