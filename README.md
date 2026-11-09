cat > README.md <<'EOF'
# Docker Containerized Web Application

A Python Flask web application packaged and deployed using Docker and Docker Compose. This project demonstrates containerization, application isolation, secure container configuration, port mapping, and health monitoring.

## Architecture

Client (localhost:8080)
        |
        v
Docker port mapping (8080:5000)
        |
        v
Docker container
        |
        v
Gunicorn application server
        |
        v
Python Flask application

## Technologies

- Python 3.12
- Flask 3.1.2
- Gunicorn 23.0.0
- Docker
- Docker Compose

## Project Structure

docker-containerized-web-app/
├── app.py
├── requirements.txt
├── Dockerfile
├── compose.yaml
├── .dockerignore
└── README.md

## Application Endpoints

| Endpoint | Description |
|---|---|
| `/` | Returns application information and environment |
| `/health` | Returns application health status |

## Run Locally with Docker

Build the image and start the container:

```bash
docker compose up -d --build
