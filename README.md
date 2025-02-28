Develop a backend application using NodeJS, NestJS that can connect to a MongoDB database and consume an external API to manage user information. Implement middleware for authentication and data validation.

Core Requirements:

1. Set up a NestJS project.
2. Connect to a MongoDB database using Mongoose.
3. Consume the external API (JSONPlaceholder) for user data.
4. Implement authentication middleware to secure certain endpoints.
5. Implement data validation middleware to ensure the integrity of incoming data.
6. Create a RESTful API to handle CRUD operations for user data.

Functional Tasks:

API Integration:

1. Fetch user data from the JSONPlaceholder API.
2. Update user data back to JSONPlaceholder via HTTP requests.

Database Operations:

Store some part of the fetched user data in MongoDB for further processing.
Implement user-related operations (e.g., creating new user records internally).

Authentication Middleware:

1. Implement JWT (JSON Web Token) based authentication to secure routes (Create and Update User).
2. Validate incoming tokens and manage session states.

Data Validation:

1. Use class-validators to ensure data integrity for incoming requests.

Suggested Project Structure:

/nestjs-backend-app
|-- /src
|   |-- /config              # Configuration files and environment variables
|   |-- /users               # User module
|   |   |-- users.module.ts
|   |   |-- users.service.ts # Business logic for user management
|   |   |-- users.controller.ts # API routes for users
|   |   |-- dto               # Data Transfer Objects for user data validation
|   |       |-- create-user.dto.ts
|   |       |-- update-user.dto.ts
|   |-- /auth                # Authentication module
|   |   |-- auth.module.ts
|   |   |-- auth.service.ts   # Business logic for authentication
|   |   |-- jwt.strategy.ts   # Strategy for JWT authentication
|   |-- /common              # Common functionalities (middlewares, utilities)
|   |   |-- /middlewares
|   |       |-- auth.middleware.ts
|   |       |-- validation.middleware.ts
|-- package.json
|-- .env                    # Environment variables
|-- tsconfig.json
