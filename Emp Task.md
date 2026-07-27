# Java Developer Intern Technical Assignment

# Employee Task Management System

---

## 📖 Overview

The objective of this assignment is to build a REST API for an **Employee Task Management System** using **Spring Boot** and a relational database.

The application should allow managing employees and assigning tasks to them.

---

## ⏱ Time Limit

**90 Minutes**

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

## 2. Task Management

Create APIs to manage tasks.

### Task Fields

| Field | Type |
|--------|------|
| id | Long |
| title | String |
| description | String |
| priority | LOW / MEDIUM / HIGH |
| status | PENDING / IN_PROGRESS / COMPLETED |
| employee | Employee |

### Required APIs

```
POST   /api/tasks
GET    /api/tasks
GET    /api/tasks/{id}
PUT    /api/tasks/{id}
DELETE /api/tasks/{id}
```

---

## 3. Task Assignment

Create an API to assign a task to an employee.

### Endpoint

```
PUT /api/tasks/{taskId}/assign/{employeeId}
```

A task should be assigned to a single employee.

---

## 4. Employee Tasks

Create an API to fetch all tasks assigned to a specific employee.

### Endpoint

```
GET /api/employees/{employeeId}/tasks
```

---

## 5. Update Task Status

Create an API to update the status of a task.

### Endpoint

```
PUT /api/tasks/{taskId}/status
```

### Sample Request

```json
{
    "status": "IN_PROGRESS"
}
```

---

# Business Rules

Implement the following business rules:

- A task can be assigned to only one employee.
- A completed task cannot be updated.

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

## Task

| Field | Type |
|--------|------|
| id | Long |
| title | String |
| description | String |
| priority | LOW / MEDIUM / HIGH |
| status | PENDING / IN_PROGRESS / COMPLETED |
| employee | Employee |

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

## Task APIs

| Method | Endpoint |
|---------|----------|
| POST | /api/tasks |
| GET | /api/tasks |
| GET | /api/tasks/{id} |
| PUT | /api/tasks/{id} |
| DELETE | /api/tasks/{id} |
| PUT | /api/tasks/{taskId}/assign/{employeeId} |
| PUT | /api/tasks/{taskId}/status |
| GET | /api/employees/{employeeId}/tasks |

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

---

# Good Luck!

We are evaluating your ability to build a working Spring Boot application with clean code, proper project structure, and maintainable design.
