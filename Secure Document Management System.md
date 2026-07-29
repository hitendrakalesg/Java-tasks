# Java Developer Intern Technical Assignment

# Secure Document Management System

---

## 📖 Overview

The objective of this assignment is to build a secure **Document Management System** using **Spring Boot**.

The application should allow users to register, log in, upload documents, and manage their own files securely using **JWT Authentication** and **Role-Based Authorization**.

Administrators should have access to all uploaded documents, while normal users should only be able to access their own documents.

---

## ⏱ Time Limit

**80 Minutes**

---

## 🛠 Technology Stack

Use the following technologies:

- Java 21
- Spring Boot
- Spring Security
- JWT Authentication
- Spring Data JPA
- Maven
- MySQL or PostgreSQL

---

# Functional Requirements

## 1. User Registration

Create an API to register a new user.

### User Fields

| Field | Type |
|--------|------|
| id | Long |
| fullName | String |
| email | String |
| password | String |
| role | ADMIN / USER |

### Endpoint

```
POST /api/auth/register
```

---

## 2. User Login

Create an API to authenticate users.

On successful authentication, generate and return a JWT token.

### Endpoint

```
POST /api/auth/login
```

---

## 3. Document Upload

Authenticated users should be able to upload documents.

### Endpoint

```
POST /api/files/upload
```

Each uploaded document should store:

| Field | Type |
|--------|------|
| id | Long |
| fileName | String |
| fileType | String |
| fileSize | Long |
| uploadedBy | User |
| uploadDate | LocalDateTime |
| filePath | String |

---

## 4. View My Documents

Authenticated users should be able to view only the documents uploaded by them.

### Endpoint

```
GET /api/files
```

---

## 5. Download Document

Authenticated users should be able to download a document.

### Endpoint

```
GET /api/files/{id}
```

A user should only be able to download their own uploaded documents.

---

## 6. Admin APIs

Administrators should be able to view all uploaded documents.

### Endpoint

```
GET /api/admin/files
```

---

# Business Rules

Implement the following rules:

- Users must be authenticated before accessing protected APIs.
- Every uploaded document must belong to one user.
- Users can only view and download their own documents.
- Administrators can view all uploaded documents.
- Store uploaded files in a local folder on the server.
- Store document information in the database.

---

# Database Design

## User

| Field | Type |
|--------|------|
| id | Long |
| fullName | String |
| email | String |
| password | String |
| role | ADMIN / USER |

---

## Document

| Field | Type |
|--------|------|
| id | Long |
| fileName | String |
| fileType | String |
| fileSize | Long |
| filePath | String |
| uploadDate | LocalDateTime |
| uploadedBy | User |

---

# API Summary

## Authentication

| Method | Endpoint |
|---------|----------|
| POST | /api/auth/register |
| POST | /api/auth/login |

---

## Document APIs

| Method | Endpoint |
|---------|----------|
| POST | /api/files/upload |
| GET | /api/files |
| GET | /api/files/{id} |

---

## Admin APIs

| Method | Endpoint |
|---------|----------|
| GET | /api/admin/files |

---

# Submission Instructions

Upload your project to a **GitHub repository**.

The repository should contain:

- Complete source code
- README.md
- pom.xml

---

# Bonus

You are free to implement any additional features that improve the application.

---

# AI Usage

You are allowed to use AI tools such as:

- ChatGPT
- Claude
- GitHub Copilot
- Gemini
- Official Documentation

During the follow-up discussion, you may be asked to explain your implementation, security configuration, JWT authentication flow, entity relationships, and authorization logic.

---

# Important Notes

- Build secure REST APIs using Spring Boot.
- Implement JWT-based authentication.
- Use role-based authorization for protected APIs.
- Organize the project using a clean folder structure.
- Keep the code clean and readable.
- Ensure the application runs successfully.
- You may use any IDE of your choice.

---

# Good Luck!

We are evaluating your ability to implement authentication, authorization, secure file handling, entity relationships, REST APIs, and clean Spring Boot architecture. We are also interested in how well you understand and explain your implementation during the follow-up discussion.
