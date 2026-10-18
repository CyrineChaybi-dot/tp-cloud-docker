# tp-cloud-docker
# Docker & GitHub Pages: Cloud Lab

A hands-on cloud project completed for the Cloud module (4th-year engineering program).
Goal: containerize a web application, orchestrate several services, and deploy it for free.

## What I built

- **Docker**: ran containers (Nginx) and built a custom image (`monapp:v1`, `monapp:v2`) from a Dockerfile.
- **Docker Compose**: a 3-service architecture (Nginx, PostgreSQL, Redis) with a persistent named volume (`pgdata`).
- **GitHub Pages**: free static website hosting.
- **Environment**: GitHub Codespaces (no local installation required).

## Live demo

https://YOUR-USERNAME.github.io/tp-cloud-docker/

## Concepts covered

| Concept | Tool |
|---|---|
| Containers and images | Docker, Dockerfile |
| Multi-container apps, networks, volumes | Docker Compose |
| Hosting (PaaS) | GitHub Pages |

## Dockerfile

```dockerfile
FROM nginx:alpine
COPY index.html /usr/share/nginx/html/index.html
EXPOSE 80
```

## Key takeaways

- An image is a template; a container is a running instance of it.
- Containers are ephemeral: important data must live in a volume.
- To change an app, rebuild a new image and replace the old container.
