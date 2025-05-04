# Full-Stack Auth App (React, Express, MongoDB Atlas, Docker Compose)

This project is a full-stack authentication application with a React frontend, Express backend, and MongoDB Atlas for the database. All services are containerized using Docker Compose.

## Features
- User signup and login
- JWT authentication
- Password hashing
- Protected dashboard route
- MongoDB Atlas cloud database
- Docker Compose orchestration
- Hot-reload/watch mode for development

## Project Structure
```
.
├── backend/
│   ├── src/
│   ├── Dockerfile
│   └── package.json
├── frontend/
│   ├── src/
│   ├── Dockerfile
│   └── package.json
├── docker-compose.yml
├── .gitignore
└── README.md
```

## Prerequisites
- [Docker](https://www.docker.com/products/docker-desktop)
- [Node.js & npm](https://nodejs.org/) (for local development)
- [MongoDB Atlas account](https://www.mongodb.com/cloud/atlas)

## Environment Variables
Create a `.env` file in the `backend/` directory:
```
MONGODB_URI=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/<database>?retryWrites=true&w=majority
JWT_SECRET=your-secret-key
PORT=4000
```

## Running with Docker Compose
1. Build and start all services:
   ```bash
   docker-compose up --build
   ```
2. Access the app:
   - Frontend: [http://localhost:3000](http://localhost:3000)
   - Backend API: [http://localhost:4000](http://localhost:4000)

## Development (Hot Reload)
- Frontend and backend containers use volume mounts for live code updates.
- Vite (frontend) and nodemon (backend) enable watch mode.

## API Endpoints
- `POST /api/auth/signup` — Register a new user
- `POST /api/auth/login` — Login and receive JWT
- `GET /api/auth/me` — Get current user (protected)

## Customization
- Update the MongoDB URI and JWT secret in your `.env` file.
- Change the database name as needed.

## License
MIT 