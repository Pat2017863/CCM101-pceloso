# Laboratory 07: The Cloud Operations Engineer

## Mission Overview

This laboratory activity focuses on monitoring a Linux server, deploying an Nginx web server using Docker, generating HTTP requests, and examining application logs and container resource usage.

## Objectives

- Check the host server's RAM, disk capacity, and CPU activity.
- Deploy an Nginx container named `client-website`.
- Generate successful HTTP requests and a 404 error.
- Analyze Docker application logs.
- Monitor CPU, memory, and network usage.
- Document the results in Markdown and maintain my GitHub portfolio.

## Monitoring Commands Executed

| Command | Purpose |
|---|---|
| `free -h` | Checks memory usage. |
| `df -h /` | Checks root filesystem storage. |
| `top` | Displays running processes and CPU activity. |
| `docker ps` | Lists running containers. |
| `curl http://localhost:8080/` | Tests the web server. |
| `docker logs client-website` | Displays container logs. |
| `docker stats client-website` | Monitors live container resources. |

## Skills Learned

- Linux system monitoring
- Docker container deployment
- HTTP testing with curl
- Application log analysis
- Container resource monitoring
- Technical documentation using Markdown
- Git and GitHub version control

## Evidence

Screenshots of the completed checkpoints are stored in the `screenshots/` folder.
