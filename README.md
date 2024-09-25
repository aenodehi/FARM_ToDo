# Todo App

This is a full-stack Todo application built using Docker Compose. The application consists of a frontend built with React, a backend built with FastAPI, and MongoDB as the database. The Nginx server is used for routing.

## A Brief view of Project Structure

```
.
├── backend/
│   ├── Dockerfile
│   ├── requirements.txt
│   └── src/
│       └── server.py
├── frontend/
│   ├── Dockerfile
│   ├── package.json
│   ├── public/
│   └── src/
│       └── App.js
├── nginx/
│   └── nginx.conf
├── .gitignore
└── compose.yaml
```

## Prerequisites

- Docker
- Docker Compose

## Setup Instructions

### 1. Clone the Repository

```bash
git clone <repository-url>
cd <repository-directory>
```

### 2. Build and Start the Services

Run the following command to build and start the services:

```bash
docker-compose up --build
```

### 3. Access the Application

- **Frontend**: Open your browser and navigate to `http://localhost:3000`.
- **Backend API**: You can use tools like `curl` or Postman to send requests to `http://localhost:8001`.
- **Nginx**: Open your browser and navigate to `http://localhost:8000` to see if Nginx is serving the frontend or backend correctly.

## Configuration

### Environment Variables

Ensure you have a `.env` file in the root directory with the necessary environment variables. Example:

```env
MONGO_URI=mongodb://username:password@mongodb:27017/dbname
```
