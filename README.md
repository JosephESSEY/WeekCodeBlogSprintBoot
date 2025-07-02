# Blog Personal API - Spring Boot

Welcome to the **Blog Personal** project developed with Spring Boot. This API provides a scalable and secure blogging platform with full CRUD functionality for articles, users, categories, and comments.

## Project Goals

* Enable users to create, read, update, and delete blog articles
* Manage users, roles, and permissions
* Organize articles by category
* Allow visitors to comment on articles
* Deliver a robust, secure, and well-structured API

## Main Features

* User authentication and authorization with Spring Security + JWT
* CRUD operations for **Articles**
* CRUD operations for **Users**
* CRUD operations for **Comments**
* CRUD operations for **Categories**
* JPA/Hibernate ORM for database persistence
* Input validation with Bean Validation (Jakarta Validation)
* Exception handling with Spring ControllerAdvice
* API pagination and filtering
* CORS and other security features

## Database Tables

The API uses the following relational database tables:

* **users**

  * id
  * name
  * email
  * password (hashed)
  * role
  * created\_at

* **articles**

  * id
  * title
  * content
  * image
  * created\_at
  * updated\_at
  * category\_id (foreign key)
  * user\_id (foreign key, author)

* **categories**

  * id
  * name
  * description

* **comments**

  * id
  * content
  * created\_at
  * user\_id (author)
  * article\_id (target)

## Technologies Used

* Java
* Spring Boot
* Spring Data JPA (Hibernate)
* PostgreSQL or MySQL
* Spring Security + JWT
* Maven
* JUnit / Mockito for testing

## Installation

1. Clone the repository:

```bash
git clone https://github.com/your-user/blog-personal-springboot.git
```

2. Import the project in your IDE (IntelliJ, Eclipse, etc.)

3. Configure application properties in `src/main/resources/application.properties` or `application.yml`:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/your_db
spring.datasource.username=your_user
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
jwt.secret=your_jwt_secret
```

4. Build the project:

```bash
mvn clean install
```

5. Run the application:

```bash
mvn spring-boot:run
```

## Testing

Run the tests with:

```bash
mvn test
```

## Notes

* This Spring Boot backend uses **Spring Data JPA (Hibernate)** for all database persistence.
* Input validation, security, and exception handling are properly implemented.
* This project is part of three separate repositories:

  * Laravel (PHP)
  * Express.js (Node)
  * Spring Boot (Java)

---
