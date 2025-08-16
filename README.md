# 3-Tier Application

## Overview

This project is a 3-tier application consisting of a Client Side (React),
Node.js Service, and Python Service with a PostgreSQL database.
The client application communicates with the Node.js service, which in turn communicates with the Python service to handle data operations. 
The goal is to have a functional application where the client can interact with a list of elements that updates in real-time.

## Project Structure

- `client/`: Contains the React client application.
- `node-service/`: Contains the Node.js service.
- `python-service/`: Contains the Python service with PostgreSQL integration.

## Setup
##python
cd python-service
uvicorn app.main:app --reload
##postgreSQL
DATABASE_URL = "postgresql://postgres:1234567@localhost:5432/fastapi_db"
##react
cd react-client
npm start
##node.js
cd node_service
node index.js
##docker
docker-compose up -d

### Prerequisites

- Node.js (v21.5.0 or compatible)
- Python (3.x)
- PostgreSQL
- Git

### Installation

1. **Clone the Repository**

   ```bash
    https://github.com/Neenu-T/Three-tier-App.git
    cd Three-tier-App

## Technologies Used

- **Node.js**: Backend API and WebSocket server.
- **Express**: Web framework for Node.js.
- **Python**: Backend data handling with FastAPI.
- **PostgreSQL**: Database for storing data.
- **React**: Front-end user interface.
- **Docker**: Containerization for deployment.

## Setup and Installation

### Prerequisites

- Docker: Make sure Docker is installed and running on your machine.
- Docker Compose: Install Docker Compose if not included with Docker.

### Setup

1. **Clone the repository:**
   ```bash
   https://github.com/Neenu-T/Three-tier-App.git
   cd Three-tier-App
   ```

2. **Build and run the application:**
   ```bash
   docker-compose up --build
   ```

3. **Access the application:**
   - Client: `http://localhost`
   - Node.js Service: `http://localhost:3001`
   - Python Service: `http://localhost:9000`
   - PostgreSQL: Port `5433` on the host

## Services

- **client**: React frontend (served by Nginx)
- **node_service**: Node.js backend (Express)
- **python_service**: Python FastAPI API
- **postgres**: PostgreSQL database

## Configuration

- Ports and environment variables are set in `docker-compose.yml`.
- Change ports or service URLs there if needed.

## Useful Commands

- View logs:
  ```bash
  docker-compose logs
  ```
- Stop services:
  ```bash
  docker-compose down
  ```

## Troubleshooting

- If a port is already in use, change the host port in `docker-compose.yml`.
- Check logs for errors using `docker-compose logs`.

## File Structure

```
client/           # React frontend
node_service/     # Node.js backend
python-service/   # Python FastAPI service
docker-compose.yml
```
