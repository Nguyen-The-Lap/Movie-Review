# Movie Review Application (Spring Boot)

Welcome to the **Spring Boot Movie Review Application**!\
This project is developed using the Spring Boot framework, offering a
robust and flexible structure for building modern web applications.

This application provides users with a platform to browse movies, read
reviews, write their own reviews, and rate films. Users can also search
for movies based on various filters and criteria.\
The front-end is built using **HTML, CSS, and JavaScript**, while the
back-end uses **Spring Boot** and **PostgreSQL**. The entire system is
designed to be scalable, maintainable, and easily extendable.

------------------------------------------------------------------------

## 📦 Dependencies

### PostgreSQL (optional)

``` xml
<dependency>
    <groupId>org.postgresql</groupId>
    <artifactId>postgresql</artifactId>
    <scope>runtime</scope>
</dependency>
```

### Thymeleaf Template Engine

``` xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-thymeleaf</artifactId>
</dependency>
```

------------------------------------------------------------------------

## ⚙️ Application Configuration

Navigate to:\
`src/main/resources/application.properties`

### PostgreSQL Configuration

``` properties
spring.datasource.url=jdbc:postgresql://localhost:5432/dsi
spring.datasource.username=postgres
spring.datasource.password=root

spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
```

### Hibernate DDL Auto

``` properties
spring.jpa.hibernate.ddl-auto=update
```

------------------------------------------------------------------------

## ▶️ Running the Application

``` bash
mvn spring-boot:run
```

------------------------------------------------------------------------

## 🧰 Setup Instructions

    1. Install PostgreSQL.
    2. Default PostgreSQL username: postgres
    3. Set the PostgreSQL password to: root
    4. Create a database named `dsi`.
    5. Run the project — all required tables will be automatically created in the `dsi` database.
    6. Use the following default login credentials:

       Admin:    username `admin`,   password `admin`
       User:     username `user`,    password `user`
       Editor:   username `editor`,  password `editor`
       Creator:  username `creator`, password `creator`
