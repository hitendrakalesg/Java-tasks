# Java Developer Intern Technical Assignment

# Movie Ticket Booking System

---

## 📖 Overview

The objective of this assignment is to build a REST API for a **Movie Ticket Booking System** using **Spring Boot** and a relational database.

The application should allow managing movies, shows, and ticket bookings.

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

## 1. Movie Management

Create APIs to manage movies.

### Movie Fields

| Field | Type |
|--------|------|
| id | Long |
| title | String |
| genre | String |
| duration | Integer (Minutes) |
| language | String |

### Required APIs

```
POST   /api/movies
GET    /api/movies
GET    /api/movies/{id}
PUT    /api/movies/{id}
DELETE /api/movies/{id}
```

---

## 2. Show Management

Create APIs to manage movie shows.

### Show Fields

| Field | Type |
|--------|------|
| id | Long |
| movie | Movie |
| showDate | LocalDate |
| showTime | LocalTime |
| screenNumber | Integer |
| totalSeats | Integer |

### Required APIs

```
POST   /api/shows
GET    /api/shows
GET    /api/shows/{id}
PUT    /api/shows/{id}
DELETE /api/shows/{id}
```

---

## 3. Ticket Booking

Create an API to book a movie ticket.

### Booking Fields

| Field | Type |
|--------|------|
| id | Long |
| customerName | String |
| customerEmail | String |
| show | Show |
| seatNumber | String |
| bookingTime | Timestamp |

### Endpoint

```
POST /api/bookings
```

### Sample Request

```json
{
    "customerName": "John Doe",
    "customerEmail": "john@example.com",
    "showId": 1,
    "seatNumber": "A5"
}
```

---

## 4. View Bookings

Create APIs to view bookings.

### Get All Bookings

```
GET /api/bookings
```

### Get Booking By ID

```
GET /api/bookings/{id}
```

### Get Bookings By Show

```
GET /api/shows/{showId}/bookings
```

---

## 5. Cancel Booking

Create an API to cancel a booking.

### Endpoint

```
DELETE /api/bookings/{bookingId}
```

---

# Business Rules

Implement the following business rules:

- A seat can only be booked once for a particular show.
- A movie must exist before creating a show.
- A show must exist before booking a ticket.
- A booking must belong to one show only.

---

# Database Design

## Movie

| Field | Type |
|--------|------|
| id | Long |
| title | String |
| genre | String |
| duration | Integer |
| language | String |

---

## Show

| Field | Type |
|--------|------|
| id | Long |
| movie | Movie |
| showDate | LocalDate |
| showTime | LocalTime |
| screenNumber | Integer |
| totalSeats | Integer |

---

## Booking

| Field | Type |
|--------|------|
| id | Long |
| customerName | String |
| customerEmail | String |
| show | Show |
| seatNumber | String |
| bookingTime | Timestamp |

---

# API Summary

## Movie APIs

| Method | Endpoint |
|---------|----------|
| POST | /api/movies |
| GET | /api/movies |
| GET | /api/movies/{id} |
| PUT | /api/movies/{id} |
| DELETE | /api/movies/{id} |

---

## Show APIs

| Method | Endpoint |
|---------|----------|
| POST | /api/shows |
| GET | /api/shows |
| GET | /api/shows/{id} |
| PUT | /api/shows/{id} |
| DELETE | /api/shows/{id} |

---

## Booking APIs

| Method | Endpoint |
|---------|----------|
| POST | /api/bookings |
| GET | /api/bookings |
| GET | /api/bookings/{id} |
| GET | /api/shows/{showId}/bookings |
| DELETE | /api/bookings/{bookingId} |

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

We are evaluating your ability to design entity relationships, implement business rules, build clean REST APIs, and write maintainable Spring Boot applications.
