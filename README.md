**English** | [Español](README_ES.md)

# B-Ganos Management System

## Overview

B-Ganos is a Java desktop-based transactional management system designed for the administration of a recreational botanical garden and its associated retail store.

The system implements a multilayer architecture with relational persistence and supports two persistence strategies: DAO-based and JPA-based. It includes transaction management and concurrency control mechanisms.

All domain entities, business logic and user interface are implemented in Spanish, as the project was developed in a Spanish academic context.

This project was developed in the context of the Software Modeling course (3th year, Software Engineering, Universidad Complutense de Madrid, 2024–2025) by a 12-member team.

This repository represents a maintained copy of the original collaborative project.


## Architecture

The application follows a strict multilayer architecture:

- Presentation Layer → Java Swing graphical interface  
- Business Layer → Application services and business logic  
- Integration Layer → Persistence and data access  
- Relational Database Layer → SQL schema definition (.sql)

Key architectural concerns addressed:

- Transaction management  
- Concurrency control  
- Clear separation between business objects and transfer objects (depending on version)  
- Pattern-oriented layered design → Design guided by established software patterns

---

## Implemented Versions

### 1. DAO-Based Persistence

- Direct relational persistence using SQL/MySQL
- Implementation of:
  - Data Access Object (DAO)
  - Transfer Object
  - Transfer Object Assembler
  - Application Service
  - Service to Worker
  - Custom queries

In this version, the business layer operates using Transfer Objects.

---

### 2. JPA-Based Persistence

- Persistence using JPA (Java Persistence API)
- Domain-based persistence using JPA
- Business Object pattern integration
- EclipseLink recommended as provider

In this version, the business layer operates using Domain Business Objects, improving modularity and separation of concerns.

---

## Design Patterns Applied

- Service to Worker  
- Application Service  
- Data Access Object  
- Transfer Object  
- Transfer Object Assembler  
- Business Object  
- Domain Store  

Note: Patterns applied follow course requirements and illustrate layered architecture design.

---

## Technologies Used

- Java  
- Swing  
- MySQL  
- SQL (.sql schema)  
- JPA 2.x  
- EclipseLink  
- JUnit  
- Git  

---

## Project Structure

```
├── Presentation Layer
├── Business Layer
├── Integration Layer
```

Folder names remain in Spanish as in the original implementation.
Each layer is structurally isolated to ensure maintainability and separation of responsibilities.

---

## Core Functionalities

### Greenhouse Management

- Invoice lifecycle management
- Ticket management
- Greenhouse administration
- Irrigation system management
- Plant management
- Manufacturer management
- Analytical queries (e.g., highest ticket sales dates per greenhouse)

---

### Store Management

- Product and brand management
- Supplier management
- Sales lifecycle management
- Employee and shift management
- Inventory updates
- Sales processing and returns

---

## Testing

Unit testing was implemented using JUnit, covering:

- Business logic validation  
- Persistence behavior  
- Critical transactional flows  

---

## UML Modeling

The UML diagrams were created following IBM RSAD standards.

The complete UML design documentation (class diagrams, sequence diagrams, component diagrams and deployment diagrams) is available in a separate repository:
https://github.com/melanydece/BGanos-UML-modeling

---

## Team

Developed collaboratively by a 12-member team.

The full list of contributors can be found in the repository's "Contributors" section.