# Task Manager API

A Spring Boot RESTful API for task management with JWT authentication.

## Features

- **Task Management**
  - Create, read, update, and delete tasks
  - Mark tasks as complete
  
- **Authentication & Authorization**
  - JWT-based authentication
  - Role-based access control (future implementation)
  
- **API Documentation**
  - Swagger/OpenAPI documentation
  
- **Error Handling**
  - Global exception handling
  - Standardized error responses

## Technology Stack

- **Backend**
  - Java 17
  - Spring Boot 3.2.0
  - Spring Security
  - Spring Data JPA (Hibernate)
  - H2 Database (in-memory)
  
- **Tools**
  - Gradle
  - Swagger/OpenAPI 3.0
  - Lombok

## API Documentation

The API is documented using Swagger UI. After starting the application, access:

- Swagger UI: `http://localhost:8080/swagger-ui.html`
- OpenAPI Docs: `http://localhost:8080/v3/api-docs`

### Authentication

Endpoints (except `/api/auth/**`) require JWT authentication. Include the token in the `Authorization` header:

```
Authorization: Bearer <your_token>
```

## Setup

### Prerequisites

- Java 17 JDK
- Gradle

### Running the Application

1. Clone the repository
2. Build the project:
   ```bash
   ./gradlew build
   ```
3. Run the application:
   ```bash
   ./gradlew bootRun
   ```

The application will start on `http://localhost:8080`

## Testing

Run all tests:
```bash
./gradlew test
```

### Test Coverage

- **Unit Tests**: Service layer with mocked dependencies
- **Integration Tests**: Controller endpoints with real database
- **Exception Handling**: Global exception scenarios

## Database Access

When running in development:

- H2 Console: `http://localhost:8080/h2-console`
- JDBC URL: `jdbc:h2:mem:taskdb`
- Username: `sa`
- Password: (leave empty)

## Future Improvements

- Add user roles and permissions
- Implement task assignment
- Add due dates and priorities
- Containerize with Docker
