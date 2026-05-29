# Spring Boot + PostgreSQL — Docker Demo

REST API built with Spring Boot and PostgreSQL, fully containerized with Docker.

## Tech Stack
- Java 17
- Spring Boot
- PostgreSQL 15
- Docker & Docker Compose

## How to run

```bash
docker compose up
```

Then hit: `http://localhost:8080/products`

## Architecture
- `app` container: Spring Boot REST API on port 8080
- `db` container: PostgreSQL database
- Containers communicate via Docker Compose internal network
- Data persists via Docker volume

## Endpoints
| Method | URL | Description |
|---|---|---|
| GET | /products | Returns all products |

## What I learned
- Multi-stage Docker builds to reduce image size
- Docker Compose networking — services communicate by name
- Volume persistence so data survives container restarts