# Dockerized Node.js + React Application

This project demonstrates a Dockerized setup for a full-stack application with a React frontend and Node.js/Express backend. The application runs in separate containers managed by Docker Compose.

## 🛠 Prerequisites

1. **Docker** installed on your system:
   - [Docker Desktop for Windows/Mac](https://www.docker.com/products/docker-desktop)
   - [Docker Engine for Linux](https://docs.docker.com/engine/install/)

2. Basic understanding of:
   - Node.js and Express (for backend)
   - React (for frontend)
   - Docker concepts (containers, images, volumes)

## 📚 Docker Basics

1. **Dockerfile**: A blueprint for building Docker images
2. **Docker Image**: A packaged application with its dependencies
3. **Docker Container**: A running instance of an image
4. **Docker Compose**: Tool for defining and running multi-container applications
5. **Volumes**: Persistent storage for containers
6. **Port Mapping**: Connecting host ports to container ports

📦 Key Docker commands:
- `docker build -t <name> .` - Build an image from a Dockerfile
- `docker run -p <host>:<container> <image>` - Run a container
- `docker-compose up` - Start services defined in docker-compose.yml
- `docker ps` - List running containers
- `docker-compose down` - Stop all containers

## Getting Started

1. Clone this repository
 git clone git@github.com:TaranaGit/Dockerized-Node.js-React-Demo.git
 cd Dockerized-Node.js-React-Demo

## Running the Application

To start both frontend and backend services:

```bash
docker-compose up --build
```
This will:

Build images for both frontend and backend

Create and start two containers

Map ports:

Frontend: localhost:3000

Backend: localhost:4000

After startup, you can access:

React app: http://localhost:3000

Express API: http://localhost:4000

## Development Workflow

During development:
The frontend container uses npm start which typically includes hot-reloading

The backend container uses nodemon for automatic restarts on file changes

Both services use volume mounts for live code updates:

Changes to local files are reflected in the containers