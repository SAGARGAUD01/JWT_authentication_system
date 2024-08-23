# JWT Authentication System with Public API Microservice
## Project Overview
This project demonstrates how to build a JWT (JSON Web Token) authentication system using Node.js. The system is split into two main components:

## Main Service: Handles user authentication and authorization using JWT, manages user registration, login, and candidate information.
Public API Microservice: Provides a public API accessible via API keys, allowing access to user profiles and candidate data without traditional email/password authentication.
Features
User Authentication and Authorization:

Register users with hashed passwords.
Log in users and generate JWT tokens.
Protect certain routes using JWT authentication.
## Candidate Management:

Add candidates to the database, associated with the currently authenticated user.
Retrieve candidates associated with the logged-in user.
## Public API Microservice:

Provides access to user profile and candidate information using an API key instead of JWT tokens.
Secured endpoints accessible via API keys.

## Main Service
This service is responsible for handling user authentication and candidate management.

Endpoints
## User Authentication Endpoints:

POST /api/register: Register a new user.
POST /api/login: Log in an existing user and receive a JWT token.
POST /api/protected: Access a protected route (JWT token required).
Candidate Management Endpoints:

POST /api/candidate: Add a new candidate (JWT token required).
GET /api/candidate: Retrieve candidates for the currently authenticated user (JWT token required).
Public API Microservice
This service provides public access to user profiles and candidate information using API keys.

Endpoints
## Profile Endpoints:
POST /api/public/profile: Retrieve user profile information using an API key.
Candidate Endpoints:
GET /api/public/candidate: Retrieve all candidates associated with a user using an API key.
Getting Started
Prerequisites
> Node.js
> MongoDB

## Future Improvements
Implement rate-limiting for the Public API.
Add API key management (generate, revoke keys).
Implement logging and monitoring for enhanced observability.
Add testing with tools like Jest.
