# Java Developer Intern Technical Assignment

# Banking Management System

---

## 📖 Overview

The objective of this assignment is to build a REST API for a **Banking Management System** using **Spring Boot** and a relational database.

The application should allow creating customer accounts and performing basic banking operations such as deposits, withdrawals, fund transfers, and transaction history.

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

## 1. Customer Management

Create APIs to manage customers.

### Customer Fields

| Field | Type |
|--------|------|
| id | Long |
| fullName | String |
| email | String |
| phone | String |

### Required APIs

```
POST   /api/customers
GET    /api/customers
GET    /api/customers/{id}
PUT    /api/customers/{id}
DELETE /api/customers/{id}
```

---

## 2. Account Management

Each customer can have one or more bank accounts.

### Account Fields

| Field | Type |
|--------|------|
| id | Long |
| accountNumber | String |
| accountType | SAVINGS / CURRENT |
| balance | Decimal |
| customer | Customer |

### Required APIs

```
POST   /api/accounts
GET    /api/accounts
GET    /api/accounts/{id}
GET    /api/customers/{customerId}/accounts
```

---

## 3. Deposit Money

Create an API to deposit money into an account.

### Endpoint

```
POST /api/accounts/{accountId}/deposit
```

### Sample Request

```json
{
    "amount": 5000
}
```

---

## 4. Withdraw Money

Create an API to withdraw money from an account.

### Endpoint

```
POST /api/accounts/{accountId}/withdraw
```

### Sample Request

```json
{
    "amount": 2500
}
```

---

## 5. Transfer Money

Create an API to transfer money between two accounts.

### Endpoint

```
POST /api/accounts/transfer
```

### Sample Request

```json
{
    "fromAccountId": 1,
    "toAccountId": 2,
    "amount": 1500
}
```

---

## 6. Transaction History

Create an API to retrieve all transactions for an account.

### Endpoint

```
GET /api/accounts/{accountId}/transactions
```

---

# Database Design

## Customer

| Field | Type |
|--------|------|
| id | Long |
| fullName | String |
| email | String |
| phone | String |

---

## Account

| Field | Type |
|--------|------|
| id | Long |
| accountNumber | String |
| accountType | SAVINGS / CURRENT |
| balance | Decimal |
| customer | Customer |

---

## Transaction

| Field | Type |
|--------|------|
| id | Long |
| account | Account |
| transactionType | DEPOSIT / WITHDRAW / TRANSFER |
| amount | Decimal |
| transactionDate | Timestamp |

---

# Business Rules

Implement the following business rules:

- An account cannot have a negative balance.
- Money cannot be transferred to the same account.
- Both source and destination accounts must exist before transferring money.
- Every deposit, withdrawal, and transfer should be recorded as a transaction.

---

# API Summary

## Customer APIs

| Method | Endpoint |
|---------|----------|
| POST | /api/customers |
| GET | /api/customers |
| GET | /api/customers/{id} |
| PUT | /api/customers/{id} |
| DELETE | /api/customers/{id} |

---

## Account APIs

| Method | Endpoint |
|---------|----------|
| POST | /api/accounts |
| GET | /api/accounts |
| GET | /api/accounts/{id} |
| GET | /api/customers/{customerId}/accounts |

---

## Banking APIs

| Method | Endpoint |
|---------|----------|
| POST | /api/accounts/{accountId}/deposit |
| POST | /api/accounts/{accountId}/withdraw |
| POST | /api/accounts/transfer |
| GET | /api/accounts/{accountId}/transactions |

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

We are evaluating your ability to design entity relationships, implement business rules, build REST APIs, and organize a maintainable Spring Boot application. Write clean, readable, and well-structured code.
