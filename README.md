# 🎬 Movie Review Application (Spring Boot)

Welcome to the **Spring Boot Movie Review Application**! 
A modern, full-stack project designed to deliver a clean and engaging platform for browsing movies, reading reviews, writing your own, and rating films.

Built with:

* **Spring Boot** for a powerful and scalable backend
* **PostgreSQL** as the database
* **HTML, CSS, JavaScript** for the frontend

This application is crafted to be **maintainable**, **extendable**, and suitable for real-world expansion.

---

## 📦 Dependencies

### 🐘 PostgreSQL (optional)

```xml
<dependency>
    <groupId>org.postgresql</groupId>
    <artifactId>postgresql</artifactId>
    <scope>runtime</scope>
</dependency>
```

### 🍃 Thymeleaf Template Engine

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-thymeleaf</artifactId>
</dependency>
```

---

## ⚙️ Application Configuration

Navigate to:
`src/main/resources/application.properties`

### 🔧 PostgreSQL Configuration

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/dsi
spring.datasource.username=postgres
spring.datasource.password=root

spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
```

### 🗃️ Hibernate DDL Auto

```properties
spring.jpa.hibernate.ddl-auto=update
```

---

## ▶️ Running the Application

```bash
mvn spring-boot:run
```

---

## 🧰 Setup Instructions

1. Install PostgreSQL.
2. Default PostgreSQL username: **postgres**
3. Set the PostgreSQL password to: **root**
4. Create a database named `dsi`.
5. Run the project — all required tables will be automatically created in the `dsi` database.
6. Use the following default login credentials:

```
Admin:    username admin,   password admin
User:     username user,    password user
Editor:   username editor,  password editor
Creator:  username creator, password creator
```

---

✨ Enjoy exploring and expanding your movie review platform!
