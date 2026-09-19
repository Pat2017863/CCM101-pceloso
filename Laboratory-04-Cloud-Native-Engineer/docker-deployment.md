# Docker Deployment

## Docker Version

Docker version 29.1.3, build 29.1.3-0ubuntu3~24.04.2

docker --version

# Checkpoint 5 - The Container Lifecycle

## 1. List Running Containers

### Command

```bash
docker ps
```

This command lists all Docker containers that are currently running.

## 2. Stop the Running Container

### Command

```bash
docker stop <container-id>
```

This command stops the selected running Docker container.

## 3. Verify It Is Stopped

### Command

```bash
docker ps -a
```

This command shows all containers and verifies that the stopped container has an `Exited` status.

## 4. Remove the Container Completely

### Command

```bash
docker rm <container-id>
```

This command removes the selected Docker container completely.

### Verification

```bash
docker ps -a
```

The removed container no longer appears in the list.
