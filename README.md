# Employee Management System - Spring Boot Application

## Overview

This is a Spring Boot application for managing employee data, including their projects, departments, and insurance information. The application connects to a MySQL database named `employeedb` and provides RESTful APIs for CRUD operations on four main entities.

## Entities

1. **Employee**
   - Stores employee personal and professional information
   - Related to Department, Project, and Insurance entities

2. **Project**
   - Tracks project details that employees are assigned to
   - Many-to-many relationship with Employee

3. **Department**
   - Organizes employees into functional groups
   - One-to-many relationship with Employee

4. **Insurance**
   - Manages employee insurance policies
   - One-to-one relationship with Employee

## Prerequisites

Before running the application, ensure you have:

- Java JDK 11 or later
- Maven 3.6.0 or later
- MySQL Server 5.7 or later
- IDE (IntelliJ IDEA, Eclipse, or VS Code recommended)

## Database Configuration

The application is configured to connect to a MySQL database named `employeedb`. Update the following properties in `application.properties` or `application.yml` as needed:

```properties
spring.application.name=day6
spring.datasource.url=jdbc:mysql://localhost:3306/employeedb
spring.datasource.username=root
spring.datasource.password=
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.hibernate.ddl-auto=create
```

## Setup Instructions

1. Clone the repository:
   ```bash
   git clone [repository-url]
   ```

2. Navigate to the project directory:
   ```bash
   cd employee-spring-boot-app
   ```

3. Build the project:
   ```bash
   mvn clean install
   ```

4. Run the application:
   ```bash
   mvn spring-boot:run
   ```

The application will start on port 8080 (default).

## API Endpoints

### Employee Endpoints
- `GET /api/employees` - Get all employees
- `GET /api/employees/{id}` - Get employee by ID
- `POST /api/employees` - Create new employee
- `PUT /api/employees/{id}` - Update employee
- `DELETE /api/employees/{id}` - Delete employee

### Project Endpoints
- `GET /api/projects` - Get all projects
- `GET /api/projects/{id}` - Get project by ID
- `POST /api/projects` - Create new project
- `PUT /api/projects/{id}` - Update project
- `DELETE /api/projects/{id}` - Delete project

### Department Endpoints
- `GET /api/departments` - Get all departments
- `GET /api/departments/{id}` - Get department by ID
- `POST /api/departments` - Create new department
- `PUT /api/departments/{id}` - Update department
- `DELETE /api/departments/{id}` - Delete department

### Insurance Endpoints
- `GET /api/insurances` - Get all insurance records
- `GET /api/insurances/{id}` - Get insurance by ID
- `POST /api/insurances` - Create new insurance
- `PUT /api/insurances/{id}` - Update insurance
- `DELETE /api/insurances/{id}` - Delete insurance

## Testing

The application includes unit tests and integration tests. To run all tests:

```bash
mvn test
```

## Swagger Documentation

After starting the application, you can access the Swagger UI at:
```
http://localhost:8080/swagger-ui.html
```

