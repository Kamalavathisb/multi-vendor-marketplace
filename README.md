# 🛒 Multi-Vendor Marketplace

A full-stack **Multi-Vendor E-Commerce Marketplace** built with **Django REST Framework and React**.

The platform allows multiple vendors to create and manage their own stores while customers can browse products, maintain a multi-vendor cart, place orders, make secure payments, track orders, and submit reviews.

---

## 🌐 Live Demo

🚀 **Live Website:**  
https://multi-vendor-marketplace-eight.vercel.app/

🔗 **Backend API:**  
https://multi-vendor-marketplace-uypd.onrender.com

📂 **GitHub Repository:**  
https://github.com/Kamalavathisb/multi-vendor-marketplace

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
