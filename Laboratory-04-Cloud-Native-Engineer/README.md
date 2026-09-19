# Laboratory 04 - The Cloud-Native Engineer

## Mission Overview

This laboratory introduced containerization and Docker. The activity focused on understanding the difference between traditional Virtual Machines and containers and deploying an Nginx web server using Docker.

## Objectives

- Differentiate Virtual Machines and containers.
- Access a Docker-enabled KillerCoda environment.
- Execute fundamental Docker commands.
- Pull and run an Nginx container.
- Manage the lifecycle of a Docker container.
- Document Docker operations using Markdown.

## Docker Commands Executed

```bash
docker --version
docker info
docker pull nginx
docker run -d --name nginx-server -p 8080:80 nginx
curl http://localhost:8080
docker ps
docker stop nginx-server
docker ps -a
docker rm nginx-server


