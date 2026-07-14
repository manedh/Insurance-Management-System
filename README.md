# Insurance Management System — Sawai Associates

A Full Stack Insurance Management System developed using **Java 17**, **Spring Boot**, **Spring Data JPA**, **MySQL (XAMPP)**, and **Vanilla HTML/CSS/JavaScript**.

---

# Tech Stack

| Layer | Technology |
|-------|------------|
| Backend | Java 17, Spring Boot 3.2.5, Spring Data JPA |
| Database | MySQL (XAMPP) |
| Frontend | HTML5, CSS3, JavaScript (Fetch API) |
| API Documentation | Swagger / OpenAPI |
| Build Tool | Maven |

---

# Features

- User Login Authentication
- Role-Based Access (ADMIN & AGENT)
- Customer Management (CRUD)
- Policy Management (CRUD)
- Lead Management (CRUD)
- Search Customers, Policies and Leads
- REST APIs
- MySQL Database Integration
- Swagger API Documentation
- Global Exception Handling

---

# Project Structure

```
insurance-management-system/
│
├── pom.xml
├── README.md
├── insurance_db.sql
│
└── src/
    └── main/
        ├── java/com/sawai/insurance/
        │
        ├── InsuranceManagementApplication.java
        ├── config/
        ├── controller/
        ├── dto/
        ├── entity/
        ├── exception/
        ├── repository/
        └── service/
        │
        └── resources/
            ├── application.properties
            └── static/
                ├── index.html
                ├── home.html
                ├── customers.html
                ├── policies.html
                ├── leads.html
                ├── style.css
                └── app.js
```

---

# Prerequisites

- Java JDK 17+
- Maven 3.8+
- XAMPP
- MySQL (via XAMPP)

---

# Database Setup (XAMPP)

1. Start **Apache** and **MySQL** from XAMPP Control Panel.

2. Open phpMyAdmin:

```
http://localhost/phpmyadmin
```

3. Create database:

```sql
CREATE DATABASE insurance_db;
```

4. Import the provided database file:

```
insurance_db.sql
```

or

Click

```
insurance_db
→ Import
→ Choose insurance_db.sql
→ Go
```

---

# MySQL Configuration

Open:

```
src/main/resources/application.properties
```

Default XAMPP configuration:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/insurance_db?createDatabaseIfNotExist=true

spring.datasource.username=root
spring.datasource.password=

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

**Note:** If you have set a password for MySQL in XAMPP, update:

```properties
spring.datasource.password=YOUR_PASSWORD
```

---

# Running the Project

### IntelliJ IDEA

Open the project

```
File
→ Open
→ insurance-management-system
```

Run

```
InsuranceManagementApplication.java
```

OR

### Command Line

```
mvn spring-boot:run
```

---

# Application URL

```
http://localhost:8081
```

Login Page

```
http://localhost:8081/index.html
```

---

# Default Users

| Username | Password | Role |
|----------|----------|------|
| admin | admin123 | ADMIN |
| agent | agent123 | AGENT |

---

# Authentication Token

After login, the API returns a token.

Send the token in every request:

```
X-Auth-Token
```

---

# REST APIs

## Authentication

POST

```
/api/auth/login
```

---

## Customers

```
GET     /api/customers

GET     /api/customers/{id}

GET     /api/customers/search?q=

POST    /api/customers

PUT     /api/customers/{id}

DELETE  /api/customers/{id}
```

---

## Policies

```
GET

POST

PUT

DELETE

SEARCH
```

---

## Leads

```
GET

POST

PUT

DELETE

SEARCH
```

---

# Authorization Rules

ADMIN

- GET
- POST
- PUT
- DELETE

AGENT

- GET
- POST
- PUT

AGENT cannot DELETE resources.

---

# Swagger API Documentation

Open

```
http://localhost:8081/swagger-ui.html
```

OpenAPI

```
http://localhost:8081/v3/api-docs
```

---

# Frontend Pages

- index.html
- home.html
- customers.html
- policies.html
- leads.html

---

# Build Project

```
mvn clean install
```

---

# Database Included

This project includes:

```
insurance_db.sql
```

Import this file into MySQL before running the application.

---

# Notes

- Built using Spring Boot MVC Architecture.
- Uses Spring Data JPA with MySQL.
- Frontend communicates with backend using Fetch API.
- Global Exception Handling implemented.
- Role-Based Authentication implemented.
- Database tested using XAMPP MySQL.
- Project follows Controller → Service → Repository architecture.

---

# Developed By

Dhanshri Shankar Mane

Software Developer Assignment

BTech Loan Wala LLP
