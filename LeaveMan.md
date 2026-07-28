# Java Developer Intern Technical Assignment

# Leave Management System

---

## 📖 Overview

The objective of this assignment is to build a REST API for a **Leave Management System** using **Spring Boot** and a relational database.

The application should allow employees to apply for leave, while administrators can review, approve, or reject leave requests.

---

## ⏱ Time Limit

**75 Minutes**

---

## 🛠 Technology Stack

Use the following technologies:

- Java 17 or Java 21
- Spring Boot
- Spring Data JPA
- Maven
- MySQL or PostgreSQL

---

# Functional Requirements

## 1. Employee Management

Create APIs to manage employees.

### Employee Fields

| Field | Type |
|--------|------|
| id | Long |
| name | String |
| email | String |
| department | String |

### Required APIs

```
POST   /api/employees
GET    /api/employees
GET    /api/employees/{id}
PUT    /api/employees/{id}
DELETE /api/employees/{id}
```

---

## 2. Leave Management

Create APIs to manage leave requests.

### Leave Fields

| Field | Type |
|--------|------|
| id | Long |
| employee | Employee |
| leaveType | SICK / CASUAL / ANNUAL |
| fromDate | LocalDate |
| toDate | LocalDate |
| reason | String |
| status | PENDING / APPROVED / REJECTED |

---

## 3. Apply Leave

Create an API for an employee to apply for leave.

### Endpoint

```
POST /api/leaves
```

### Sample Request

```json
{
    "employeeId": 1,
    "leaveType": "CASUAL",
    "fromDate": "2026-08-10",
    "toDate": "2026-08-12",
    "reason": "Family Function"
}
```

---

## 4. View Leave Requests

### Get All Leave Requests

```
GET /api/leaves
```

### Get Leave Request By ID

```
GET /api/leaves/{id}
```

### Get Leave Requests of an Employee

```
GET /api/employees/{employeeId}/leaves
```

---

## 5. Approve Leave

Create an API to approve a leave request.

### Endpoint

```
PUT /api/leaves/{leaveId}/approve
```

---

## 6. Reject Leave

Create an API to reject a leave request.

### Endpoint

```
PUT /api/leaves/{leaveId}/reject
```

---

# Business Rules

Implement the following business rules:

- An employee cannot apply for overlapping leave dates.
- Leave can only be approved or rejected if its current status is **PENDING**.
- A leave request must belong to one employee.
- An employee must exist before applying for leave.

---

# Database Design

## Employee

| Field | Type |
|--------|------|
| id | Long |
| name | String |
| email | String |
| department | String |

---

## Leave Request

| Field | Type |
|--------|------|
| id | Long |
| employee | Employee |
| leaveType | SICK / CASUAL / ANNUAL |
| fromDate | LocalDate |
| toDate | LocalDate |
| reason | String |
| status | PENDING / APPROVED / REJECTED |

---

# API Summary

## Employee APIs

| Method | Endpoint |
|---------|----------|
| POST | /api/employees |
| GET | /api/employees |
| GET | /api/employees/{id} |
| PUT | /api/employees/{id} |
| DELETE | /api/employees/{id} |

---

## Leave APIs

| Method | Endpoint |
|---------|----------|
| POST | /api/leaves |
| GET | /api/leaves |
| GET | /api/leaves/{id} |
| GET | /api/employees/{employeeId}/leaves |
| PUT | /api/leaves/{leaveId}/approve |
| PUT | /api/leaves/{leaveId}/reject |

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

During the follow-up discussion, you may be asked to explain your implementation and design decisions.

---

# Important Notes

- Follow REST API best practices.
- Keep the project organized and readable.
- Use meaningful class, method, and variable names.
- Ensure the application runs successfully.
- You may use any IDE of your choice.

---

# Good Luck!

We are evaluating your ability to design entity relationships, implement business rules, build REST APIs, and write clean, maintainable Spring Boot applications.
