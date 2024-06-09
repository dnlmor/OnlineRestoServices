# OnlineRestoServices

# Status
Work in progress

# Project Overview
The Online Restaurant Service project aims to develop a microservices-based online platform for managing restaurant operations such as user management, menu management, order processing, payment handling, and notifications. The system is designed to be scalable, modular, and easy to deploy using Docker containers.

# Project Structure
    OnlineRestoServices/
    │
    ├── ORS-APIGateway/
    │   ├── app/
    │   ├── Dockerfile
    │   ├── requirements.txt
    │   └── run.py
    ├── ORS-MenuService/
    │   ├── app/
    │   ├── Dockerfile
    │   ├── requirements.txt
    │   └── run.py
    ├── ORS-OrderService/
    │   ├── app/
    │   ├── Dockerfile
    │   ├── requirements.txt
    │   └── run.py
    ├── ORS-PaymentService/
    │   ├── app/
    │   ├── Dockerfile
    │   ├── requirements.txt
    │   └── run.py
    ├── ORS-NotificationService/
    │   ├── app/
    │   ├── Dockerfile
    │   ├── requirements.txt
    │   └── run.py
    ├── ORS-ServiceDiscovery/
    │   ├── app/
    │   ├── Dockerfile
    │   ├── requirements.txt
    │   └── run.py
    └── ORS-UserService/
        ├── app/
        ├── Dockerfile
        ├── requirements.txt
        └── run.py

# Project Components
- API Gateway: Entry point for all client requests. It routes requests to the appropriate microservices
- User Service: Handles user management operations such as registration, login, and profile management
- Menu Service: Manages restaurant menus, including adding, updating, and deleting items
- Order Service: Handles order processing, including creating, updating, and canceling orders
- Payment Service: Integrates payment processing functionality for handling payments from users
- Notification Service: Sends notifications to users for order updates, promotions, etc
- Service Discovery: Provides service discovery functionality for enabling dynamic service registration and discovery

# Setup and Deployment
To deploy the project locally using Docker:
    - Ensure Docker and Docker Compose are installed on your system
    - Clone the project repository
    - Navigate to the project root directory
    - Run 'docker-compose up --build' to build and start all services

# Additional Notes
Each microservice has its own directory containing its source code, Dockerfile, and dependencies. The api-gateway service acts as a single entry point for all client requests and routes them to the appropriate microservice. Ensure proper port mappings in the docker-compose.yml file to avoid port conflicts.