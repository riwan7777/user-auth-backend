# User Authentication Backend

A simple Node.js backend for user registration, login, and protected routes using JWT and MongoDB.

## Features

- User Registration (with password hashing using bcrypt)
- User Login (returns a JWT token)
- Protected route (accessible only with a valid token)

## Technologies Used

- Node.js
- Express.js
- MongoDB (with Mongoose)
- JWT (jsonwebtoken)
- bcryptjs
- dotenv

## Setup Instructions

1. Clone the repository
2. Run npm install to install dependencies
3. Create a .env file in the root with the following:

MONGO_URI=your_mongodb_connection_string  
JWT_SECRET=your_jwt_secret

4. Run the server:

node server.js

## API Endpoints

### Register
POST /api/auth/register  
Body:
{
  "username": "rizwan",
  "email": "rizwan@example.com",
  "password": "test123"
}

### Login
POST /api/auth/login  
Body:
{
  "email": "rizwan@example.com",
  "password": "test123"
}

### Protected Route
GET /api/auth/profile  
Header:
Authorization: <token>

## Author

Rizwan (PPP Internship Phase Project)