# Docker Administration

Container infrastructure reference for production Docker environments. Covers engine configuration, multi-service orchestration, networking architecture, and operational hardening across development and production contexts.

## Topics

| Area | Details |
|---|---|
| Engine Configuration | Daemon options, storage drivers, logging, resource constraints |
| Compose Orchestration | Multi-service stacks, dependency graphs, environment management |
| Networking | Custom bridge networks, DNS resolution, cross-host connectivity |
| Volume Management | Named volumes, bind mounts, backup and restore procedures |
| Registry Operations | Push/pull workflows, private registry setup, image tagging strategies |
| Production Patterns | Health checks, restart policies, secret injection, rolling deployments |

## Structure

```
├── compose/              # Multi-service Compose stacks
├── dockerfiles/          # Production-hardened Dockerfiles
├── networking/           # Custom network configurations
├── volumes/              # Volume management examples
└── ops/                  # Operational runbooks and scripts
```

## Usage

```bash
docker compose -f compose/<stack>.yml up -d
docker compose logs -f
docker compose down --volumes
```
