# Airbnb Clone Project

## Project Overview

The Airbnb Clone Project is a backend system that replicates core Airbnb features such as user management, property listings, bookings, payments, and reviews. The goal is to build a scalable and secure platform that handles real-world rental workflows. Key objectives include secure user authentication, efficient property and booking management, integrated payment processing, and user review functionality. The project is built using a modern tech stack that includes Django, Django REST Framework, PostgreSQL, GraphQL, Celery, Redis, Docker, and CI/CD pipelines for automated testing and deployment.

---

## Team Roles

| Role               | Responsibilities                                                                 |
|--------------------|----------------------------------------------------------------------------------|
| Backend Developer  | API development, business logic, database schemas                                |
| Database Admin     | Schema design, optimization, and management                                      |
| DevOps Engineer    | CI/CD setup, monitoring, deployment                                               |
| QA Engineer        | Functional and performance testing                                               |

---

## Technology Stack
- **Django**: Web framework for backend services
- **Django REST Framework**: API development
- **GraphQL**: Flexible API queries
- **PostgreSQL**: Relational database
- **Celery**: Asynchronous task handling
- **Redis**: Caching and session management
- **Docker**: Containerized environment
- **CI/CD Pipelines**: Automated testing and deployment

---

## Database Design

The Airbnb Clone project relies on a relational database structure to manage users, properties, bookings, payments, and reviews. Below are the key entities and their relationships:


### Users
- `id`: Unique identifier for each user  
- `name`: Full name of the user  
- `email`: Unique email for authentication  
- `password_hash`: Securely stored password  
- `role`: Host or Guest  

### Properties
- `id`: Unique property identifier  
- `title`: Name of the property  
- `description`: Details about the listing  
- `location`: Address or coordinates  
- `owner_id`: References the user who owns the property  

### Bookings
- `id`: Unique booking identifier  
- `user_id`: References the guest who made the booking  
- `property_id`: References the booked property  
- `start_date`: Booking start date  
- `end_date`: Booking end date  

### Payments
- `id`: Unique payment identifier  
- `booking_id`: References the associated booking  
- `amount`: Payment amount  
- `payment_date`: Date of payment  
- `status`: Paid, pending, or failed  

### Reviews
- `id`: Unique review identifier  
- `user_id`: References the guest leaving the review  
- `property_id`: References the property being reviewed  
- `rating`: Numerical score  
- `comment`: Textual feedback

### Entity Relationships
- A **User** can own multiple **Properties**  
- A **User** can make multiple **Bookings**  
- A **Booking** is associated with one **User** (Guest) and one **Property**  
- A **Payment** is linked to one **Booking**  
- A **Review** is written by a **User** and linked to one **Property**

---
