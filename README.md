# Knowledge Sharing Platform – Backend
CDAC 2026 Assignment

##  Project Overview

This is the backend for the Knowledge Sharing Platform with AI Assist.

The platform allows users to:
- Register and login using JWT authentication
- Create, edit, and delete their own articles
- View and search public articles
- Use AI-powered content improvement and summary generation

Tech Stack:
- Java 17
- Spring Boot
- Spring Security (JWT Authentication)
- MySQL
- JPA / Hibernate

---

##  Architecture Overview

The backend follows a layered architecture:

Controller Layer  
→ Handles HTTP requests and responses

Service Layer  
→ Contains business logic (article creation, authorization checks, AI handling)

Repository Layer  
→ JPA repositories for database operations

Security Layer  
→ JWT Authentication filter  
→ Role-based access control  
→ Only authors can edit/delete their own articles

Authentication Flow:
1. User logs in with email + password
2. JWT token is generated
3. Token is sent in Authorization header
4. JWT filter validates token for protected routes

---

##  Folder Structure

```
src/main/java/com/project/
│
├── controller/
├── service/
├── repository/
├── entity/
├── dto/
├── config/
└── security/
```

---

##  Features Implemented

### Authentication
- User Signup
- User Login (JWT based)
- Password encryption (BCrypt)
- Secure endpoints

### Article Management
- Create article
- Edit article (Only author)
- Delete article (Only author)
- View single article
- View all articles

### Search & Filter
- Search by title
- Search by content
- Search by tags
- Filter by category

### AI Features
- Improve article content
- Generate article summary
- Suggest better title

(Mock AI supported with structure ready for real API integration)

---

##  AI Usage (Mandatory Section)

AI tools used during development:
- ChatGPT

Where AI helped:
- Designing JWT authentication flow
- Generating initial Spring Boot boilerplate
- Creating entity relationships
- Writing repository queries
- Debugging CORS issues
- Improving exception handling
- Structuring AI service logic

Manual Improvements Done:
- Refined authorization logic
- Secured endpoints properly
- Improved error responses
- Optimized database relationships
- Validated role-based access control manually

AI was used as a productivity assistant, but all logic was reviewed, tested, and refined manually.

---

##  Setup Instructions

### Prerequisites
- Java 17+
- MySQL 8+
- Maven
- IDE (IntelliJ / VS Code)

---

### 1️⃣ Database Setup

Create a MySQL database:

```sql
CREATE DATABASE knowledge_platform;
```

Update `application.properties`:

```
spring.datasource.url=jdbc:mysql://localhost:3306/knowledge_platform
spring.datasource.username=your_username
spring.datasource.password=your_password
```

---

###  Run Backend

Inside project folder:

```
mvn clean install
mvn spring-boot:run
```

Application runs on:
```
http://localhost:8080
```

---

##  Environment Variables

JWT Secret and expiration can be configured in:

```
application.properties
```

Example:

```
app.jwt.secret=your_secret_key
app.jwt.expiration=86400000
```

---

##  API Testing

You can test APIs using:
- Postman
- Thunder Client
- Swagger (if enabled)

---

##  Assignment Goals Achieved

✔ Proper layered architecture  
✔ JWT authentication  
✔ Role-based authorization  
✔ AI-assisted endpoints  
✔ Clean project structure  
✔ Secure and scalable design  

---

##  Developed By

Bhargavi Thorat  
CDAC 2026 Assignment
