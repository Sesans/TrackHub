# TrackHub
TrackHub is a web application that allows users to explore, interact with, and contribute to a curated collection of music. Users can like songs, comment, and annotate lyrics. It is designed with a microservices architecture to promote scalability and maintainability.

## 🎯 Objective
This project was created to study and apply core concepts of backend development using microservices, REST API, event-driven communication, JWT authentication, CI/CD pipelines, Docker orchestration, and modular frontend/backend integration.


## Architecture Overview

TrackHub consists of the following microservices:

 - `auth-service` - Handles user registration, login, JWT authentication, and role-based access.

 - `music-service` - Manages music publishing, search with pagination, likes, comments, and annotations.

 - `notification-service` - Sends confirmation emails via RabbitMQ when a user registers. Future features include handling password change notifications and SMS integration.

 - `api-gateway` - Routes all requests to the correct microservice and handles CORS/security.

 - `frontend` - JavaScript frontend that consumes the API to render the TrackHub user interface.

Each service is containerized and orchestrated via Docker Compose.

## Features

- User registration and login with JWT

-  Publish and list songs

-  Like, comment, and annotate song lyrics

-  Infinite scroll with pageable songs

-  Confirmation email on user registration (via RabbitMQ)

-  Personalized song recommendations (planned)

-  Centralized API Gateway

### Technologies Used

- Java 17 + Spring Boot

- Spring Security + JWT

- PostgreSQL

- RabbitMQ

- JavaScript in frontend

- Docker + Docker Compose

## 🚀 Getting Started

To run the full application with Docker:

git clone https://github.com/your-username/trackhub.git
cd trackhub
docker-compose up --build

Each service will be available on its designated port. The frontend will be accessible at http://localhost:5500 (or as configured).

    Ensure ports 8080, 5432, 5500 are free.