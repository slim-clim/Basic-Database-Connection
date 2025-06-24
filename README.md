# Simple REST API with Express.js and PostgreSQL

## Project Overview

This project is a Simple RESTful API built using Express.js that performs CRUD operations (Create, Read, Update, Delete) on a PostgreSQL `users` table. It demonstrates the basics of REST API development, including database connection, error handling, and modular code structure.

## Prerequisites

Before running this project, ensure you have the following installed:

- Node.js (Recommended version: 16+)
- npm (Node Package Manager)
- PostgreSQL
- A code editor (VS Code recommended)
- Thunder Client (Optional, for API testing)

## Installation & Setup Steps

1. Clone the repository

git clone <your-repo-url>
cd mini-rest-api

2.  Initialize Node.js project

npm init -y

3.  Install dependencies

npm install express pg dotenv
npm install nodemon

4.  Set up your PostgreSQL database:

Create a database, e.g. users_database

Run the SQL:

CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  name VARCHAR(100),
  email VARCHAR(100),
  age INTEGER
);

5.  Create .env file (refer to .env.example)

PORT=5000
DATABASE_HOST=localhost
DATABASE_USER=postgres
DATABASE_PASSWORD=your_password
DATABASE_NAME=users_db
DATABASE_PORT=5432


6.  Run the server

npm start

7.  View the project

Server runs on: http://localhost:5000

##  Technologies Used

-   Node.js

-   Express.js

-   PostgreSQL

-   JavaScript

-   Thunder Client (for API testing)

##  Project Structure

expressandpostgresql/
    controller/
        users.js
    database/
        index.js
    images/
        image.png
        image-1.png
        image-2.png
        image-3.png
        image-4.png
        image-5.png
        image-6.png
    middleware/
        errorHandler.js
    routes/
        users.js
    app.js
    package.json
    .env
    README.md


##  Features
-   Full CRUD (Create, Read, Update, Delete) functionality

-   Global error handling

-   Input Validation

-   404 handling for invalid routes

-   Modular structure for cleaner code

-   Thunder Client Collection available for easy testing

##  API Endpoints with visual proof with Thunder Client
### GET /
Returns: Hello, World!

![GET / endpoint](/images/image.png)

### GET /users
Returns all users.

![GET /users endpoint](/images/image-2.png)

### GET /users/:id
Returns a user by ID.

![GET /users/:id endpoint](/images/image-3.png)

### POST /users

Creates a new user. Request Body:
{
    "name": "Ochanya Godwin",
    "email": "ochanyagodwin2027@yahoo.com",
    "age": 24
}

![POST /users endpoint](/images/image-1.png)

### PUT /users/:id

Updates an existing user. Request Body:
{
    "name": "Godwin Oche",
    "email": "ochegodwin@gmail.com",
    "age": 25
}

![PUT /users/:id endpoint](/images/image-4.png)

### DELETE /users/:id
Deletes the user with the given ID.

![DELETE /users/:id enpoint](/images/image-5.png)

### Error Handling

-   400 Bad Request: Missing or invalid data

-   404 Not Found: Resource not found

-   500 Internal Server Error: Unexpected issue on the server

### Example package.json Script
"scripts": {
  "start": "nodemon app.js"
}

## Visual Proof of postgreSQL GUI with pgadmin

![Visual Proof of postgreSQL GUI with pgadmin](/images/image-6.png)


##  Author

Godwin Oche
