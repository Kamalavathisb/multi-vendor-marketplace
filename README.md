# 🛒 Multi-Vendor Marketplace

A full-stack **Multi-Vendor E-Commerce Marketplace** built with **Django REST Framework and React**.

The platform allows multiple vendors to create and manage their own stores while customers can browse products, maintain a multi-vendor cart, place orders, make secure payments, track orders, and submit reviews.

---

## 🚀 Project Overview

This project demonstrates the development of a modern e-commerce platform with separate experiences for:

* 👤 Buyers
* 🏪 Vendors
* 👨‍💼 Administrators

The application includes authentication, role-based access control, product management, shopping cart functionality, order processing, payments, reviews, analytics, and vendor management.

---

## ✨ Key Features

### 👤 Buyer Features

* 🔐 User registration and authentication
* 🔎 Product search and filtering
* ↕️ Product sorting
* 🛍️ Multi-vendor shopping cart
* 📦 Product variants
* ❤️ Wishlist
* 💳 Secure Stripe checkout
* 🎟️ Coupon support
* 🚚 Order tracking
* ⭐ Product reviews and ratings
* 📷 Review photo uploads
* 👍 Helpful review voting
* 🚩 Review reporting

### 🏪 Vendor Features

* 📝 Vendor application
* 📦 Product CRUD operations
* 🖼️ Product image management
* 🔄 Product variants
* 📋 Order management
* 🚚 Shipping and tracking management
* 📊 Revenue analytics
* 💰 Commission tracking
* 💸 Payout requests
* ⭐ Customer review management
* 🏬 Store customization

### 👨‍💼 Admin Features

* 📊 Admin dashboard
* 📈 Platform statistics and KPIs
* 🏪 Vendor approval and management
* 📦 Product moderation
* 🛒 Order management
* ⭐ Review moderation
* 💰 Commission management
* 💸 Payout processing
* ⚙️ Platform settings

---

## 🏗️ Architecture

```text
                    ┌─────────────────────┐
                    │      React UI       │
                    │      Frontend       │
                    └──────────┬──────────┘
                               │
                               │ REST API
                               ▼
                    ┌─────────────────────┐
                    │   Django REST API   │
                    │      Backend        │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              │                │                │
              ▼                ▼                ▼
        PostgreSQL          Redis           Cloudinary
          Database          Cache          Media Storage
                               │
                               ▼
                            Celery
                         Background Tasks
```

---

## 🛠️ Tech Stack

### Backend

| Technology            | Purpose               |
| --------------------- | --------------------- |
| Python                | Backend programming   |
| Django                | Web framework         |
| Django REST Framework | REST API development  |
| Simple JWT            | Authentication        |
| PostgreSQL            | Database              |
| Redis                 | Caching               |
| Celery                | Background tasks      |
| Stripe                | Payment processing    |
| Cloudinary            | Image/media storage   |
| WhiteNoise            | Static file serving   |
| Gunicorn              | Production server     |
| django-filter         | API filtering         |
| CORS Headers          | Cross-origin requests |

### Frontend

| Technology      | Purpose              |
| --------------- | -------------------- |
| React           | Frontend development |
| Vite            | Frontend build tool  |
| Material UI     | UI components        |
| Redux Toolkit   | State management     |
| RTK Query       | API data fetching    |
| React Router    | Routing              |
| Axios           | HTTP requests        |
| Chart.js        | Analytics charts     |
| React Hook Form | Form handling        |
| Yup             | Form validation      |
| Notistack       | Notifications        |
| Day.js          | Date handling        |

---

## 📂 Project Structure

```text
multi-vendor-marketplace/
│
├── backend/
│   ├── manage.py
│   ├── requirements.txt
│   ├── .env.example
│   ├── render.yaml
│   │
│   ├── core/
│   ├── accounts/
│   ├── vendors/
│   ├── products/
│   ├── orders/
│   ├── reviews/
│   └── analytics/
│
├── frontend/
│   ├── index.html
│   ├── package.json
│   ├── vite.config.js
│   │
│   └── src/
│       ├── components/
│       ├── pages/
│       ├── features/
│       ├── services/
│       └── ...
│
└── README.md
```

---

## 🔐 Authentication & Authorization

The application uses **JWT-based authentication**.

Different users have different permissions based on their role:

```text
                    User
                     │
          ┌──────────┼──────────┐
          │          │          │
          ▼          ▼          ▼
        Buyer      Vendor      Admin
          │          │          │
       Shopping   Store       Platform
       Orders     Management  Management
```

### Authentication Features

* JWT access tokens
* Refresh tokens
* Secure authentication
* Role-based access control
* Protected API endpoints

---

## 🛍️ Marketplace Workflow

### Buyer Workflow

```text
Register/Login
      ↓
Browse Products
      ↓
Search / Filter
      ↓
Add Products to Cart
      ↓
Review Cart
      ↓
Apply Coupon
      ↓
Stripe Checkout
      ↓
Order Created
      ↓
Track Order
      ↓
Submit Review
```

### Vendor Workflow

```text
Vendor Application
        ↓
Admin Approval
        ↓
Create Store
        ↓
Add Products
        ↓
Product Approval
        ↓
Receive Orders
        ↓
Manage Shipping
        ↓
Track Revenue
        ↓
Request Payout
```

---

## 💳 Payment Processing

The project integrates **Stripe** for secure payment processing.

```text
Customer
   │
   ▼
Shopping Cart
   │
   ▼
Checkout
   │
   ▼
Stripe Payment
   │
   ▼
Payment Confirmation
   │
   ▼
Order Creation
```

---

## 📊 Vendor Analytics

Vendors can monitor their business performance through analytics dashboards.

Analytics include:

* Revenue
* Orders
* Sales performance
* Commission
* Payout information
* Product performance

Charts are implemented using **Chart.js**.

---

## 🔌 REST API

The backend provides RESTful APIs for different application modules.

### Main API Areas

```text
/api/accounts/
/api/vendors/
/api/products/
/api/orders/
/api/reviews/
/api/analytics/
```

The API supports:

* Authentication
* CRUD operations
* Filtering
* Searching
* Sorting
* Pagination
* Role-based permissions

---

## ☁️ Deployment Architecture

The project is designed for cloud deployment.

```text
React Frontend
      │
      ▼
   Vercel
      │
      │ REST API
      ▼
Django Backend
      │
      ▼
   Render
      │
 ┌────┼──────────────┐
 ▼    ▼              ▼
DB   Redis       Cloudinary
```

---

## ⚙️ Environment Variables

The project uses environment variables for sensitive configuration.

Example backend configuration:

```env
SECRET_KEY=
DEBUG=
DATABASE_URL=
REDIS_URL=
STRIPE_SECRET_KEY=
STRIPE_PUBLISHABLE_KEY=
CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=
```

Example frontend configuration:

```env
VITE_API_URL=
VITE_STRIPE_PUBLISHABLE_KEY=
```

> Never commit real API keys, passwords, or secret credentials to GitHub.

---

## 🧪 Testing

The backend can be tested using Django's testing framework and API testing tools.

Testing areas include:

* Authentication
* Product APIs
* Cart functionality
* Orders
* Payments
* Reviews
* Vendor management
* Admin functionality

---

## 📚 Skills Demonstrated

This project demonstrates practical experience with:

* Python
* Django
* Django REST Framework
* React
* REST APIs
* PostgreSQL
* JWT Authentication
* Redux Toolkit
* API Integration
* Role-Based Access Control
* E-Commerce Architecture
* Stripe Integration
* Redis
* Celery
* Cloudinary
* Git & GitHub
* Responsive UI Development
* Database Design

---

## 📌 Project Status

🚧 **Full-Stack E-Commerce Marketplace**

The project contains separate frontend and backend applications and demonstrates a complete multi-vendor marketplace architecture.

---

## 👩‍💻 Portfolio

### Kamalavathi S Balegar

🎓 MCA Graduate | Python Full-Stack Developer | Software Developer

**GitHub:**
https://github.com/Kamalavathisb

**LinkedIn:**
https://www.linkedin.com/in/kamalavathisb



---

<p align="center">
  Built with ❤️ using Python, Django, Django REST Framework and React
</p>
