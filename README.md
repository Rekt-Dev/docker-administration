# Docker Administration — Lab Reference

Container infrastructure reference covering production Docker engine administration: image authoring, multi-service orchestration, Swarm cluster operations, secrets management, private registry setup, and operational hardening patterns.

## Repository Structure

```
compose-labs/          # Multi-container Compose deployments
  cli-app-deployment/  # CLI app container testing patterns
  basic-compose/       # Service definition fundamentals
  drupal-postgres/     # Stateful app + DB with Nginx reverse proxy
  multi-service-stack/ # Voting app stack with Redis, worker, result service
  swarm-init/          # Compose → Swarm migration pattern
  voting-app-compose/  # Distributed voting app with custom Dockerfile

dockerfiles/           # Image authoring patterns
  nginx-basic/         # Minimal Nginx image configuration
  node-express/        # Node.js Express containerization
  multi-stage/         # Multi-stage build for reduced image size
  python-flask/        # Flask app with gunicorn entrypoint
  alpine-optimized/    # Alpine-based image with init and health signals
  node-app/            # Full Node.js app with .dockerignore and routing

monitoring/
  healthcheck-patterns/ # HEALTHCHECK instruction patterns and best practices

registry/
  private-registry/    # Self-hosted Docker Registry v2 setup

secrets/
  basic-secrets/       # Docker secrets — file-based provisioning
  swarm-secrets/       # Secrets in Swarm service definitions

swarm/
  voting-app/          # Swarm deployment of the voting application
  ops-drupal/          # Drupal + PostgreSQL Swarm stack
  stack-nginx/         # Voting stack with Nginx ingress
  stack-voting/        # Stack with build-time secrets integration
  stack-swarm-mesh/    # Compose override workflow (dev/test/prod)
  stack-secrets/       # Placement constraints and secret binding
  stack-registry/      # Registry service integrated in Swarm stack
  stack-full/          # Full voting app with routing mesh and TLS
  secrets-lab/         # Swarm secrets rotation and service redeployment
  visualizer/          # Swarm visualizer service stack

volumes/
  bind-mount/          # Bind mount workflow with live reload (Jekyll)

references/
  k8s-manifests/       # Kubernetes manifests for cross-platform context
  lecture-notes/       # kubectl cheat sheets and API change notes
  intro/               # Docker fundamentals and conceptual diagrams
```

## Key Engineering Patterns

| Pattern | Location |
|---|---|
| Multi-stage builds | `dockerfiles/multi-stage` |
| Secret injection at runtime | `secrets/swarm-secrets`, `swarm/secrets-lab` |
| Service mesh routing | `swarm/stack-swarm-mesh`, `swarm/stack-full` |
| Private registry integration | `registry/private-registry`, `swarm/stack-registry` |
| Health-aware containers | `monitoring/healthcheck-patterns` |
| Compose override workflow | `swarm/stack-swarm-mesh` |

## Prerequisites

- Docker Engine 24+
- Docker Compose v2
- Multi-node environment for Swarm labs
