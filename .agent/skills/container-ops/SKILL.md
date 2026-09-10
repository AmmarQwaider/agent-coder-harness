---
name: container-ops
description: >-
  For Docker Compose, network topology, and container isolation changes.
---

# container-ops

## Scope
Modifying Dockerfiles, `docker-compose.yml`, Kubernetes manifests, or network topology.

## Guidelines
1. **Images**: Use minimal base images (e.g., alpine or distroless) to reduce the attack surface.
2. **Privileges**: Never run containers as root unless strictly necessary. Specify a `USER` in the Dockerfile.
3. **Isolation**: Use isolated container networks. Do not expose internal service ports to the host unless required for public access.
4. **Resources**: Always define CPU and memory limits/requests for containers.

## Verification
- Run `docker compose config` to validate compose files.
- Ensure the containers build successfully and pass security scans (e.g., using Trivy or similar tools).
