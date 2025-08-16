# Three-tier App

This project is a three-tier application using Docker Compose.  
It consists of a React frontend, Node.js backend, Python FastAPI service, and PostgreSQL database.

## Services

- **client**: React frontend (served by Nginx)
- **node_service**: Node.js backend (Express)
- **python_service**: Python FastAPI API
- **postgres**: PostgreSQL database

## Prerequisites

- [Docker](https://www.docker.com/) and [Docker Compose](https://docs.docker.com/compose/) installed

## Setup & Running

1. Clone this repository.
2. Build and start all services:
   ```
   docker-compose up --build
   ```
3. Access the app:
   - Frontend: [http://localhost](http://localhost)
   - Node.js API: [http://localhost:3001](http://localhost:3001)
   - Python API: [http://localhost:9000](http://localhost:9000)
   - PostgreSQL: Host port `5433`

## Service Communication

- The frontend communicates with the Node.js backend.
- The Node.js backend proxies requests to the Python FastAPI service.
- The Python service interacts with PostgreSQL.

## Configuration

- Ports and environment variables are set in `docker-compose.yml`.
- Change ports or service URLs there if needed.

## Useful Commands

- View logs:
  ```
  docker-compose logs
  ```
- Stop services:
  ```
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
