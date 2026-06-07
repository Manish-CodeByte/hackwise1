# Neurox Backend

A Spring Boot backend developed for the Neurox Hackathon. The application provides user management, assessment evaluation, personalized learning roadmaps, module tracking, and dashboard analytics.

## Tech Stack

* Java 17
* Spring Boot 3.2.4
* Spring Data JPA
* H2 In-Memory Database
* Lombok
* Maven

## Features

* User Registration and Login
* Multiple Choice Question (MCQ) Assessment
* Concept-wise Performance Evaluation
* Personalized Learning Roadmap Generation
* Learning Module Management
* Progress Tracking
* User Dashboard Analytics

## Getting Started

### Prerequisites

* Java 17 or later
* Maven 3.8+

### Installation & Run

```bash
# Clone repository
git clone <repository-url>

# Navigate to project directory
cd neurox-backend

# Build project
mvn clean install

# Run application
mvn spring-boot:run
```

The server starts at:

```
http://localhost:8080
```

## API Endpoints

### User Management

| Method | Endpoint              | Description         |
| ------ | --------------------- | ------------------- |
| POST   | `/api/users/register` | Register a new user |
| POST   | `/api/users/login`    | Authenticate user   |

### Questions

| Method | Endpoint         | Description       |
| ------ | ---------------- | ----------------- |
| GET    | `/api/questions` | Retrieve all MCQs |

### Responses

| Method | Endpoint         | Description               |
| ------ | ---------------- | ------------------------- |
| POST   | `/api/responses` | Submit assessment answers |

### Evaluation

| Method | Endpoint                   | Description                  |
| ------ | -------------------------- | ---------------------------- |
| POST   | `/api/evaluation/{userId}` | Generate concept-wise scores |

### Learning Roadmap

| Method | Endpoint                | Description                      |
| ------ | ----------------------- | -------------------------------- |
| GET    | `/api/roadmap/{userId}` | Get recommended learning modules |

### Learning Modules

| Method | Endpoint                  | Description             |
| ------ | ------------------------- | ----------------------- |
| GET    | `/api/modules/{moduleId}` | Retrieve module details |

### Progress Tracking

| Method | Endpoint        | Description              |
| ------ | --------------- | ------------------------ |
| POST   | `/api/progress` | Mark module as completed |

### Dashboard

| Method | Endpoint                  | Description             |
| ------ | ------------------------- | ----------------------- |
| GET    | `/api/dashboard/{userId}` | Retrieve user dashboard |

## Database

The project uses an H2 in-memory database.

### H2 Console

```
http://localhost:8080/h2-console
```

### Connection Details

| Property | Value                  |
| -------- | ---------------------- |
| JDBC URL | `jdbc:h2:mem:neuroxdb` |
| Username | `sa`                   |
| Password | *(empty)*              |

## Sample Data

The application loads sample data automatically at startup:

* 10 MCQ questions
* Concepts: Java, OOP, Data Structures
* 9 Learning Modules

## Project Structure

```
src/main/java
├── controller
├── service
├── repository
├── model
├── dto
└── config
```

## Future Enhancements

* JWT Authentication
* PostgreSQL/MySQL Support
* Role-Based Access Control
* REST API Documentation (Swagger/OpenAPI)
* Analytics Dashboard Improvements
* AI-Powered Learning Recommendations

## License

This project was developed as part of the Neurox Hackathon.
