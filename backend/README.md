# Backend - Student Dropout Analysis System

## Overview
This is the backend module of the Student Dropout Analysis System built with Spring Boot.

## Technology Stack
- Java 17+
- Spring Boot 3.x
- Spring Data JPA
- MySQL Database
- Maven

## Project Structure
```
backend/
├── src/
│   ├── main/
│   │   ├── java/com/dropoutanalysis/
│   │   │   ├── controller/    # REST API Controllers
│   │   │   ├── model/         # Entity Models
│   │   │   ├── repository/    # JPA Repositories
│   │   │   ├── service/       # Business Logic
│   │   │   └── config/        # Configuration Classes
│   │   └── resources/
│   │       ├── application.properties
│   │       └── data.sql
│   └── test/
├── pom.xml
└── README.md
```

## Setup Instructions

### Prerequisites
- Java JDK 17 or higher
- Maven 3.6+
- MySQL 8.0+

### Configuration
1. Configure MySQL database in `application.properties`
2. Update database credentials
3. Run the application

### Running the Application
```bash
mvn clean install
mvn spring-boot:run
```

## API Endpoints
API documentation will be available at: `http://localhost:8080/api`

## Features
- Student Profile Management
- Data Upload and Validation
- Dashboard Analytics
- Risk Scoring and Prediction
- Role-based Access Control
