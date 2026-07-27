# Java Developer Intern Technical Assignment

# Role-Based Authentication System using Spring Boot & JWT

---

## Overview

The objective of this assignment is to build a secure REST API using Spring Boot, Spring Security, JWT, and a relational database (MySQL or PostgreSQL).

The application should support authentication and role-based authorization for two types of users:

- ADMIN
- USER

---

## Time Limit

2 Hours 30 Minutes

---

## Technology Stack

Use the following technologies:

- Java 17 or Java 21
- Spring Boot
- Spring Security
- Spring Data JPA
- JWT
- Maven
- MySQL or PostgreSQL

---

# Functional Requirements

## 1. Register User

Create an API to register a new user.

### Endpoint

```
POST /api/auth/register
```

### Sample Request

```json
{
  "fullName": "John Doe",
  "email": "john@example.com",
  "password": "Password123",
  "role": "USER"
}
```

The application should store the user information in the database.

---

## 2. Login

Create an API that authenticates a user.

### Endpoint

```
POST /api/auth/login
```

### Sample Request

```json
{
  "email": "john@example.com",
  "password": "Password123"
}
```

### Expected Response

```json
{
  "token": "<jwt_token>"
}
```

The generated JWT token should be used to access protected APIs.

---

## 3. Protected APIs

### USER Dashboard

```
GET /api/user/dashboard
```

This endpoint should only be accessible to users with the **USER** role.

---

### ADMIN Dashboard

```
GET /api/admin/dashboard
```

This endpoint should only be accessible to users with the **ADMIN** role.

---

### Profile API

```
GET /api/profile
```

Return the details of the currently authenticated user.

Both ADMIN and USER should be able to access this endpoint.

---

# Database

Create a User entity with the following fields.

| Field | Type |
|--------|------|
| id | Long |
| fullName | String |
| email | String |
| password | String |
| role | ADMIN / USER |
| createdAt | Timestamp |

---

# API Summary

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | /api/auth/register | Register user |
| POST | /api/auth/login | Login |
| GET | /api/profile | Logged-in user profile |
| GET | /api/user/dashboard | USER Dashboard |
| GET | /api/admin/dashboard | ADMIN Dashboard |

---

# Submission

Upload the project to GitHub.

The repository should include:

- Source code
- README.md
- pom.xml

---

# Bonus (Optional)

You are free to implement any additional features that improve the application.

---

# AI Usage

You may use AI tools (ChatGPT, Claude, GitHub Copilot, Gemini, etc.) while completing this assignment.

During the follow-up discussion, you may be asked to explain your implementation and design decisions.

---

# Good Luck!

Write clean, maintainable code and build a secure REST API that satisfies the requirements above.
