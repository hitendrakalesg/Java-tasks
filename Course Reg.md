# Java Developer Intern Technical Assignment

# Course Registration System

---

## 📖 Overview

The objective of this assignment is to build a REST API for a **Course Registration System** using **Spring Boot** and a relational database.

The application should allow managing students, courses, and course enrollments.

---

## ⏱ Time Limit

**60 Minutes**

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

## 1. Student Management

Create APIs to manage students.

### Student Fields

| Field | Type |
|--------|------|
| id | Long |
| name | String |
| email | String |
| department | String |

### Required APIs

```
POST   /api/students
GET    /api/students
GET    /api/students/{id}
PUT    /api/students/{id}
DELETE /api/students/{id}
```

---

## 2. Course Management

Create APIs to manage courses.

### Course Fields

| Field | Type |
|--------|------|
| id | Long |
| courseName | String |
| courseCode | String |
| instructor | String |
| credits | Integer |

### Required APIs

```
POST   /api/courses
GET    /api/courses
GET    /api/courses/{id}
PUT    /api/courses/{id}
DELETE /api/courses/{id}
```

---

## 3. Course Enrollment

Create an API to enroll a student in a course.

### Endpoint

```
POST /api/enrollments
```

### Sample Request

```json
{
    "studentId": 1,
    "courseId": 2
}
```

---

## 4. Get Student Courses

Create an API to fetch all courses enrolled by a student.

### Endpoint

```
GET /api/students/{studentId}/courses
```

---

## 5. Get Course Students

Create an API to fetch all students enrolled in a course.

### Endpoint

```
GET /api/courses/{courseId}/students
```

---

## 6. Cancel Enrollment

Create an API to remove a student's enrollment from a course.

### Endpoint

```
DELETE /api/enrollments/{enrollmentId}
```

---

# Business Rules

Implement the following business rules:

- A student cannot enroll in the same course more than once.
- A student and course must exist before enrollment.
- An enrollment can only belong to one student and one course.

---

# Database Design

## Student

| Field | Type |
|--------|------|
| id | Long |
| name | String |
| email | String |
| department | String |

---

## Course

| Field | Type |
|--------|------|
| id | Long |
| courseName | String |
| courseCode | String |
| instructor | String |
| credits | Integer |

---

## Enrollment

| Field | Type |
|--------|------|
| id | Long |
| student | Student |
| course | Course |
| enrolledAt | Timestamp |

---

# API Summary

## Student APIs

| Method | Endpoint |
|---------|----------|
| POST | /api/students |
| GET | /api/students |
| GET | /api/students/{id} |
| PUT | /api/students/{id} |
| DELETE | /api/students/{id} |

---

## Course APIs

| Method | Endpoint |
|---------|----------|
| POST | /api/courses |
| GET | /api/courses |
| GET | /api/courses/{id} |
| PUT | /api/courses/{id} |
| DELETE | /api/courses/{id} |

---

## Enrollment APIs

| Method | Endpoint |
|---------|----------|
| POST | /api/enrollments |
| GET | /api/students/{studentId}/courses |
| GET | /api/courses/{courseId}/students |
| DELETE | /api/enrollments/{enrollmentId} |

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

We are evaluating your ability to build a working Spring Boot application, model relationships between entities, implement the required business rules, and write clean, maintainable code.
