# OnlineRestoServices

# Status
Work in progress

# Project Overview
The Online Restaurant Service project aims to develop a microservices-based online platform for managing restaurant operations such as user management, menu management, order processing, payment handling, and notifications. The system is designed to be scalable, modular, and easy to deploy using Docker containers.

# File Project Structure Backend

        OnlineRestoServices/
        │
        ├── ORS-APIGateway/
        │   ├── app/
        │   │   ├── __init__.py
        │   │   ├── routes.py
        │   │   ├── models.py
        │   │   ├── controllers.py
        │   │   ├── services.py
        │   │   └── utils.py
        │   ├── Dockerfile
        │   ├── requirements.txt
        │   ├── config.py
        │   ├── run.py
        │   └── tests/
        │       ├── __init__.py
        │       ├── test_routes.py
        │       ├── test_models.py
        │       └── test_services.py
        │
        ├── ORS-MenuService/
        │   ├── app/
        │   │   ├── __init__.py
        │   │   ├── routes.py
        │   │   ├── models.py
        │   │   ├── controllers.py
        │   │   ├── services.py
        │   │   └── utils.py
        │   ├── Dockerfile
        │   ├── requirements.txt
        │   ├── config.py
        │   ├── run.py
        │   └── tests/
        │       ├── __init__.py
        │       ├── test_routes.py
        │       ├── test_models.py
        │       └── test_services.py
        │
        ├── ORS-OrderService/
        │   ├── app/
        │   │   ├── __init__.py
        │   │   ├── routes.py
        │   │   ├── models.py
        │   │   ├── controllers.py
        │   │   ├── services.py
        │   │   └── utils.py
        │   ├── Dockerfile
        │   ├── requirements.txt
        │   ├── config.py
        │   ├── run.py
        │   └── tests/
        │       ├── __init__.py
        │       ├── test_routes.py
        │       ├── test_models.py
        │       └── test_services.py
        │
        ├── ORS-PaymentService/
        │   ├── app/
        │   │   ├── __init__.py
        │   │   ├── routes.py
        │   │   ├── models.py
        │   │   ├── controllers.py
        │   │   ├── services.py
        │   │   └── utils.py
        │   ├── Dockerfile
        │   ├── requirements.txt
        │   ├── config.py
        │   ├── run.py
        │   └── tests/
        │       ├── __init__.py
        │       ├── test_routes.py
        │       ├── test_models.py
        │       └── test_services.py
        │
        ├── ORS-NotificationService/
        │   ├── app/
        │   │   ├── __init__.py
        │   │   ├── routes.py
        │   │   ├── models.py
        │   │   ├── controllers.py
        │   │   ├── services.py
        │   │   └── utils.py
        │   ├── Dockerfile
        │   ├── requirements.txt
        │   ├── config.py
        │   ├── run.py
        │   └── tests/
        │       ├── __init__.py
        │       ├── test_routes.py
        │       ├── test_models.py
        │       └── test_services.py
        │
        ├── ORS-ServiceDiscovery/
        │   ├── app/
        │   │   ├── __init__.py
        │   │   ├── routes.py
        │   │   ├── models.py
        │   │   ├── controllers.py
        │   │   ├── services.py
        │   │   └── utils.py
        │   ├── Dockerfile
        │   ├── requirements.txt
        │   ├── config.py
        │   ├── run.py
        │   └── tests/
        │       ├── __init__.py
        │       ├── test_routes.py
        │       ├── test_models.py
        │       └── test_services.py
        │
        └── ORS-UserService/
            ├── app/
            │   ├── __init__.py
            │   ├── routes.py
            │   ├── models.py
            │   ├── controllers.py
            │   ├── services.py
            │   └── utils.py
            ├── Dockerfile
            ├── requirements.txt
            ├── config.py
            ├── run.py
            └── tests/
                ├── __init__.py
                ├── test_routes.py
                ├── test_models.py
                └── test_services.py

        ├── docker-compose.yml
        └── README.md


# Why GraphQL Instead of Traditional Routes?

Flexibility: GraphQL provides a more flexible and efficient way to fetch data compared to traditional RESTful routes. Instead of multiple endpoints, GraphQL has a single endpoint (/graphql) that handles all types of queries and mutations.

Client-driven Queries: With GraphQL, clients can request exactly the data they need, avoiding over-fetching or under-fetching of data that can happen with traditional REST endpoints.

Schema-driven Development: GraphQL is schema-driven, meaning you define types, queries, and mutations in a schema (schema.py in our case). This schema acts as a contract between the client and server, ensuring clarity and consistency in data interactions.

Type Safety: GraphQL schemas enforce type safety, ensuring that data returned from queries and mutations adheres to specified types, reducing runtime errors.

Single Endpoint: Having a single /graphql endpoint simplifies API management and documentation compared to maintaining multiple RESTful endpoints.