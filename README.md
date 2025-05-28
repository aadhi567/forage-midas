# Midas

A robust transaction processing system built with Spring Boot that handles financial transactions with incentive calculations. This project is part of the JPMC Advanced Software Engineering Forage program.

# Features
Transaction processing with Kafka integration
Incentive calculation API integration
User balance management
RESTful API for balance queries
Real-time transaction processing
Data persistence with JPA/Hibernate

# Technical Stack

Java 17
Spring Boot 3.2.5
Spring Kafka
Spring Data JPA
H2 Database
Maven
JUnit 5

#Project Structure

```
src/
├── main/
│   ├── java/
│   │   └── com/jpmc/midascore/
│   │       ├── controller/    # REST controllers
│   │       │   ├── BalanceController.java
│   │       │   ├── IncentiveController.java
│   │       │   └── TransactionController.java
│   │       ├── foundation/    # Core domain models
│   │       │   ├── Balance.java
│   │       │   ├── Incentive.java
│   │       │   ├── Transaction.java
│   │       │   └── TransactionKafkaListener.java
│   │       ├── service/       # Business logic
│   │       │   ├── IncentiveService.java
│   │       │   └── TransactionService.java
│   │       └── MidasCoreApplication.java
│   └── resources/
│       └── application.yml    # Application configuration
└── test/
    └── java/
        └── com/jpmc/midascore/
            └── TaskFiveTests.java  # Integration tests
```
# Architecture
The system follows a microservices architecture:

Main application processes transactions via Kafka
Separate Incentive API calculates transaction incentives
REST API provides balance queries
Data is persisted in H2 database

# Development

Code Style:
  
  Follows Java code conventions
  Uses Spring Boot best practices
  Includes comprehensive logging
  Proper error handling
  
Testing:

  Unit tests for core functionality
  Integration tests for API endpoints
  Kafka integration tests
