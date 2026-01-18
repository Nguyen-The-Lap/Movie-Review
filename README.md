# 🎬 Movie Review Application

A modern, full-stack **Movie Review Web Application** built using **Spring Boot MVC**, designed for browsing movies, writing reviews, rating films, and managing personalized movie lists.

This project demonstrates a complete MVC architecture with authentication, authorization, database persistence, and a responsive server-side rendered frontend.

---

## 👥 Project Information

**Project Name:** Movie Review Application
**Developed by:** Tien Dat & The Lap
**Architecture:** Spring Boot MVC

---

## ✨ Features Overview

### 🎥 User Features

* User registration and login (form-based and Google OAuth2)
* Browse and search movies with pagination
* View detailed movie information (description, cast, trailer)
* Write, edit, and read movie reviews
* Rate movies on a 1–10 scale
* Manage personal **watchlist** and **favorite movies**
* Personal dashboard for saved movies

### 🛠️ Admin Features

* User management (view, edit, delete users)
* Movie management (add, edit, delete movies)
* Actor management
* Content moderation for reviews and ratings

---

## 🧱 Application Architecture

This project follows a **layered Spring Boot MVC architecture**:

* **Controller Layer** – Handles HTTP requests and routes
* **Service Layer** – Contains business logic
* **Repository (DAO) Layer** – Manages database access using Spring Data JPA
* **Model Layer** – JPA entities representing database tables
* **View Layer** – Thymeleaf templates for server-side rendered UI

This separation of concerns improves maintainability, readability, and scalability.

---

## 🔐 Authentication & Authorization

* Implemented using **Spring Security**
* Supports **form-based login** and **Google OAuth2 login**
* Passwords are encrypted using **BCrypt**
* Role-based access control ensures secure access to endpoints

### User Roles

* **USER** – Browse movies, write reviews, manage watchlist
* **CREATOR** – Create new movie entries
* **EDITOR** – Edit movie and actor information
* **ADMIN** – Full system access and management

---

## 🗄️ Database Design

### Main Entities

* **User** – Stores user information, roles, watchlists, favorites
* **Movie** – Movie details, ratings, posters, trailers
* **Review** – User reviews and ratings
* **Actor** – Actor information and movie associations
* **Role** – User roles for authorization

### Key Relationships

* User ↔ Movie (Many-to-Many for watchlist and favorites)
* Movie ↔ Actor (Many-to-Many)
* Movie ↔ Review (One-to-Many)
* User ↔ Review (One-to-One)
* User ↔ Role (Many-to-Many)

---

## 📁 Project Structure

```
src/main/java
 ├── controller    # Handles HTTP requests
 ├── service       # Business logic
 ├── repository    # Database interaction
 ├── model         # JPA entities
 ├── security      # Authentication & authorization

src/main/resources
 ├── templates     # Thymeleaf HTML views
 ├── static        # CSS, JavaScript, images
 ├── application.properties

src/test           # Unit and integration tests
```

---

## ⚙️ Technology Stack

### Backend

* Java 11
* Spring Boot 2.5.6
* Spring MVC
* Spring Security
* Spring Data JPA
* Hibernate ORM

### Frontend

* Thymeleaf
* HTML5, CSS3, JavaScript
* Bootstrap / Custom CSS

### Database

* PostgreSQL
* Hibernate DDL Auto (schema management)

### Additional Tools

* Maven (build tool)
* OAuth2 Client (Google login)
* BCrypt (password encryption)

---

## 📦 Dependencies

### PostgreSQL

```xml
<dependency>
    <groupId>org.postgresql</groupId>
    <artifactId>postgresql</artifactId>
    <scope>runtime</scope>
</dependency>
```

### Thymeleaf

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-thymeleaf</artifactId>
</dependency>
```

---

## 🔧 Application Configuration

Edit the file:

```
src/main/resources/application.properties
```

### PostgreSQL Configuration

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/dsi
spring.datasource.username=postgres
spring.datasource.password=root

spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
spring.jpa.hibernate.ddl-auto=update
```

---

## ▶️ Running the Application

### Prerequisites

* Java 11+
* Maven
* PostgreSQL

### Steps

1. Install PostgreSQL
2. Create a database named `dsi`
3. Set PostgreSQL username to `postgres` and password to `root`
4. Run the application:

```bash
mvn spring-boot:run
```

5. The database tables will be created automatically

---

## 🔑 Default Login Accounts

| Role    | Username | Password |
| ------- | -------- | -------- |
| Admin   | admin    | admin    |
| User    | user     | user     |
| Editor  | editor   | editor   |
| Creator | creator  | creator  |

---

## 🚀 Future Enhancements

* RESTful API development
* Microservices architecture
* Redis caching for performance
* CI/CD pipeline integration
* Expanded unit and integration testing
* Mobile application support
* AI-based movie recommendation system
* Social features (comments, following users)
* Migration to Spring Boot 3 and Java 17
* React frontend and Docker containerization

---

## 📚 Learning Outcomes

This project provided hands-on experience with:

* Spring Boot MVC architecture
* JPA and Hibernate ORM
* Spring Security and OAuth2
* PostgreSQL database design
* Thymeleaf templating
* Full-stack web application development

---

## ✅ Conclusion

The Movie Review Application demonstrates a complete, secure, and scalable web platform following modern development practices. It serves as a strong foundation for real-world Spring Boot applications and future system expansion.

Thank you for exploring our project! 🎉
