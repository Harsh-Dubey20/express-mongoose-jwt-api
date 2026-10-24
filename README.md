# REST API with Express, Mongoose & JWT Auth

A robust Node.js RESTful API built with Express, MongoDB (Mongoose), and JSON Web Tokens (JWT) for secure authentication. Includes CRUD operations for two resources (`User` and `Task`) and centralized error handling.

---

## Features

- **User Authentication**: Secure user registration and login with `bcryptjs` password hashing and `JWT` tokens.
- **Task Management (CRUD)**: Create, Read, Update, and Delete tasks associated with authenticated users.
- **Middleware**:
  - `authMiddleware`: Protects private routes using JWT Bearer tokens.
  - `errorMiddleware`: Handles errors globally across the app.
- **Database Integration**: MongoDB connection using Mongoose schemas and models.

---

## Tech Stack

- **Node.js** & **Express.js**
- **MongoDB** & **Mongoose**
- **JSON Web Token (JWT)**
- **BcryptJS**
- **Dotenv**

---

## Project Structure

```text
express-jwt-api/
├── config/
│   └── db.js                 # Database connection
├── controllers/
│   ├── authController.js     # Register & Login logic
│   └── taskController.js     # Task CRUD logic
├── middleware/
│   ├── authMiddleware.js     # JWT token verification
│   └── errorMiddleware.js    # Global error handler
├── models/
│   ├── User.js               # User schema
│   └── Task.js               # Task schema (Resource 2)
├── routes/
│   ├── authRoutes.js         # /api/auth routes
│   └── taskRoutes.js         # /api/tasks routes
├── .env.example              # Sample environment variables
├── .gitignore                # Git ignore rules
├── package.json              # Project dependencies
└── server.js                 # Main entry point


##Essential : Create a .env file in the root directory:

PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
