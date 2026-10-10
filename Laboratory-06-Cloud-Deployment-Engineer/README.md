# Mission 6: The Cloud Deployment Engineer

## Mission Overview

This laboratory activity demonstrates how to deploy a private cloud storage application using Docker Compose. The project uses Nextcloud as the web application and MariaDB as the database. Both services are defined in a YAML configuration file and deployed together.

## Objectives

- Understand two-tier application architecture.
- Create a Docker Compose configuration file.
- Deploy Nextcloud and MariaDB in separate containers.
- Access the Nextcloud installation page through port 8080.
- Document the deployment process using Markdown.
- Maintain the existing GitHub Cloud Computing portfolio.

## Commands Executed

| Command | Purpose |
|---|---|
| `mkdir -p nextcloud-deployment` | Creates the deployment directory. |
| `nano docker-compose.yml` | Creates the Docker Compose configuration. |
| `docker-compose up -d` | Starts the services in the background. |
| `docker-compose ps` | Checks the status of the services. |
| `docker-compose logs --tail=50` | Displays recent container logs. |
| `docker-compose down` | Stops and removes the Compose containers and network. |
| `git add .` | Stages repository changes. |
| `git commit -m "Complete Mission 6"` | Records the changes in Git. |
| `git push origin main` | Pushes committed changes to GitHub. |

If your environment uses `docker compose` instead of `docker-compose`, use the supported form of each command.

## Skills Learned

- Understanding multi-tier application architecture.
- Writing YAML configuration files.
- Deploying multiple containers with Docker Compose.
- Accessing a web application through port mapping.
- Reading container status and logs.
- Applying Infrastructure as Code principles.
- Documenting technical work and managing a GitHub portfolio.

## Screenshots

The `screenshots/` directory contains evidence of the successful deployment, the Nextcloud installation page, and the container teardown.
