# Docker Mastery — Study Notes & Labs

Working through [Docker Mastery with Kubernetes + Swarm](https://www.udemy.com/course/docker-mastery/) by Bret Fisher. This repo tracks hands-on assignments, Compose configs, and Dockerfile experiments from the course.

## Topics Covered

- **Dockerfile fundamentals** — multi-stage builds, caching, best practices
- **Docker Compose** — multi-container apps, networking, volumes
- **Swarm mode** — orchestration, services, stacks
- **Bind mounts & volumes** — dev workflows and data persistence
- **Health checks** — container readiness and liveness
- **Voting app** — full-stack Compose example (Redis, Postgres, Python, Node, .NET)

## Repo Structure

```
dockerfile-sample-1/     # simple nginx Dockerfile
dockerfile-sample-2/     # custom app Dockerfile
compose-sample-1/        # basic Compose setup
compose-sample-2/        # multi-service with networking
compose-assignment-1/    # Compose challenge
compose-assignment-2/    # advanced Compose challenge
example-voting-app/      # multi-tier voting app
bindmount-sample-1/      # dev bind mount workflow
dockerfiles/             # misc Dockerfile experiments
```

## Prerequisites

- Docker Desktop or Docker Engine
- Docker Compose v2

## Usage

Run any sample:

```bash
cd compose-sample-2
docker compose up
```

Run the voting app:

```bash
cd example-voting-app
docker compose up
```
