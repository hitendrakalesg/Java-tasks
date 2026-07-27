# Java Developer Intern Technical Assignment

# Hospital Appointment Management System

---

## 📖 Overview

The objective of this assignment is to build a REST API for a Hospital Appointment Management System using Spring Boot and a relational database.

The system should allow managing doctors, patients, and appointments.

---

## ⏱ Time Limit

**2 Hours 30 Minutes**

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

## 1. Doctor Management

Create APIs to manage doctors.

### Fields

| Field | Type |
|--------|------|
| id | Long |
| name | String |
| specialization | String |
| experience | Integer |

### APIs

```
POST   /api/doctors
GET    /api/doctors
GET    /api/doctors/{id}
PUT    /api/doctors/{id}
DELETE /api/doctors/{id}
```

---

## 2. Patient Management

Create APIs to manage patients.

### Fields

| Field | Type |
|--------|------|
| id | Long |
| name | String |
| age | Integer |
| gender | String |
| phone | String |

### APIs

```
POST   /api/patients
GET    /api/patients
GET    /api/patients/{id}
PUT    /api/patients/{id}
DELETE /api/patients/{id}
```

---

## 3. Appointment Management

Create APIs to manage appointments.

### Fields

| Field | Type |
|--------|------|
| id | Long |
| doctor | Doctor |
| patient | Patient |
| appointmentDate | LocalDate |
| appointmentTime | LocalTime |
| status | BOOKED / COMPLETED / CANCELLED |

---

## APIs

### Book Appointment

```
POST /api/appointments
```

### Get All Appointments

```
GET /api/appointments
```

### Get Appointment by ID

```
GET /api/appointments/{id}
```

### Update Appointment

```
PUT /api/appointments/{id}
```

### Cancel Appointment

```
PUT /api/appointments/{id}/cancel
```

### Mark Appointment as Completed

```
PUT /api/appointments/{id}/complete
```

### Delete Appointment

```
DELETE /api/appointments/{id}
```

---

# Additional APIs

## Get All Appointments of a Doctor

```
GET /api/doctors/{doctorId}/appointments
```

---

## Get All Appointments of a Patient

```
GET /api/patients/{patientId}/appointments
```

---

## Get Today's Appointments

```
GET /api/appointments/today
```

---

# Database Design

## Doctor

| Field | Type |
|--------|------|
| id | Long |
| name | String |
| specialization | String |
| experience | Integer |

---

## Patient

| Field | Type |
|--------|------|
| id | Long |
| name | String |
| age | Integer |
| gender | String |
| phone | String |

---

## Appointment

| Field | Type |
|--------|------|
| id | Long |
| doctor | Doctor |
| patient | Patient |
| appointmentDate | LocalDate |
| appointmentTime | LocalTime |
| status | BOOKED / COMPLETED / CANCELLED |

---

# API Summary

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | /api/doctors | Create Doctor |
| GET | /api/doctors | Get All Doctors |
| GET | /api/doctors/{id} | Get Doctor |
| PUT | /api/doctors/{id} | Update Doctor |
| DELETE | /api/doctors/{id} | Delete Doctor |
| POST | /api/patients | Create Patient |
| GET | /api/patients | Get All Patients |
| GET | /api/patients/{id} | Get Patient |
| PUT | /api/patients/{id} | Update Patient |
| DELETE | /api/patients/{id} | Delete Patient |
| POST | /api/appointments | Book Appointment |
| GET | /api/appointments | Get All Appointments |
| GET | /api/appointments/{id} | Get Appointment |
| PUT | /api/appointments/{id} | Update Appointment |
| PUT | /api/appointments/{id}/cancel | Cancel Appointment |
| PUT | /api/appointments/{id}/complete | Complete Appointment |
| DELETE | /api/appointments/{id} | Delete Appointment |
| GET | /api/doctors/{doctorId}/appointments | Doctor Appointments |
| GET | /api/patients/{patientId}/appointments | Patient Appointments |
| GET | /api/appointments/today | Today's Appointments |

---

# Submission

Upload the complete project to GitHub.

Repository should include:

- Source Code
- README.md
- pom.xml

---

# Bonus

You are free to implement any additional features that improve the application.

---

# AI Usage

You may use AI tools (ChatGPT, Claude, GitHub Copilot, Gemini, etc.) while completing this assignment.

During the follow-up discussion, you may be asked to explain your implementation and design decisions.

---

# Good Luck!

Build a clean, well-structured REST API that satisfies the above requirements. Focus on writing maintainable code and designing the application thoughtfully.
