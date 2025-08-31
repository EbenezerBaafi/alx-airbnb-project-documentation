# Airbnb Project - Backend Requirement Specifications

This document specifies the backend requirements for three key features of the Airbnb Project: **User Authentication**, **Property Management**, and **Booking System**. It includes detailed API endpoints, input/output specifications, validation rules, and performance criteria.

---

## 1. User Authentication

### **Description**
Handles user registration, login, logout, and profile management. Ensures secure authentication using JWT and OAuth for third-party logins.

---

### **API Endpoints**

| Endpoint                          | Method | Description                       | Authentication Required |
|----------------------------------|--------|----------------------------------|--------------------------|
| `/api/auth/register`            | POST   | Register a new user             | No                       |
| `/api/auth/login`               | POST   | Log in an existing user         | No                       |
| `/api/auth/oauth/:provider`     | POST   | OAuth login via Google/Facebook | No                       |
| `/api/auth/logout`              | POST   | Log out current user            | Yes                      |
| `/api/auth/profile`             | GET    | Fetch current user profile      | Yes                      |
| `/api/auth/profile`             | PUT    | Update current user profile     | Yes                      |

---

### **Input Specifications**

#### **Register (POST /api/auth/register)**
```json
{
  "fullName": "John Doe",
  "email": "john@example.com",
  "password": "Password@123"
}
