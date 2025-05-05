# Airbnb Clone Project

## Project Overview  
A full-stack booking platform clone simulating Airbnb's core functionality.  

### Goals  
- Build a scalable web application with Django backend  
- Implement secure user authentication and payment processing  
- Design a relational database for property bookings  
- Develop CI/CD pipelines for automated testing/deployment  

### Tech Stack  
- **Backend**: Django, Django REST Framework  
- **Database**: PostgreSQL  
- **API**: GraphQL (with Graphene)  
- **DevOps**: Docker, GitHub Actions

## Team Roles  

### Backend Developer  
- Designs and implements API endpoints  
- Ensures data validation and security  

### Database Administrator  
- Models database schema  
- Optimizes queries and manages migrations  

### DevOps Engineer  
- Configures CI/CD pipelines  
- Manages deployment environments  

### QA Engineer  
- Writes automated tests  
- Performs security audits

## Technology Stack  

| Technology       | Purpose                                  |
|------------------|------------------------------------------|
| Django           | Backend framework for business logic     |
| PostgreSQL       | Relational database for complex queries  |
| GraphQL          | Flexible API queries for frontend        |
| Docker           | Containerization for consistent environments |
| GitHub Actions   | Automated testing and deployment         |

## Database Design  

### Key Entities  
**Users**  
- `user_id` (PK), `email`, `password_hash`, `phone`  
**Properties**  
- `property_id` (PK), `host_id` (FK → Users), `title`, `price`  
**Bookings**  
- `booking_id` (PK), `guest_id` (FK → Users), `property_id` (FK → Properties)  

### Relationships  
- One-to-Many: User → Properties  
- Many-to-Many: Properties ↔ Bookings (via Users)

## Feature Breakdown  

### User Management  
- Secure registration/login using JWT. Ensures data privacy.  

### Property Listings  
- CRUD operations for hosts. Core revenue driver.  

### Booking System  
- Date conflict validation. Critical for user experience.  

### Reviews  
- Rating aggregation. Builds trust in the platform.

## API Security  

### Key Measures  
- **JWT Authentication**: Verifies user identity  
- **Rate Limiting**: Prevents DDoS attacks  
- **CORS Policies**: Restricts unauthorized domains  

### Why It Matters  
- Payments: PCI compliance requires encryption  
- User Data: GDPR/NDPR compliance

## CI/CD Pipeline  

### Purpose  
Automates testing → deployment to catch errors early.  

### Tools  
- **GitHub Actions**: Runs unit/integration tests  
- **Docker**: Ensures environment consistency   
