# Docker Compose Guide

## What Does the `services:` Block Do?

The `services:` block defines the containers that make up the application. In this project, it contains two services: `database` and `app`. The database service uses MariaDB, while the app service uses Nextcloud. Docker Compose reads this configuration and manages both services together.

## How Does Nextcloud Find the Database?

The Nextcloud application uses the environment variable `MYSQL_HOST=database` to identify the database service. Docker Compose creates a network for the application, allowing the containers to communicate using their service names. The `MYSQL_DATABASE`, `MYSQL_USER`, and `MYSQL_PASSWORD` variables provide the database connection details.

## Docker Run vs. Docker Compose Up

The `docker run` command is commonly used to create and start an individual container. When an application needs multiple containers, the user may have to configure and manage each one separately.

The `docker-compose up -d` command reads the `docker-compose.yml` file and starts all the defined services in the background. This makes deployment easier because the configuration is saved in one file and can be reused.

## Infrastructure as Code

Infrastructure as Code (IaC) means defining infrastructure through configuration files instead of setting everything up manually. In this activity, the Compose YAML file describes the Nextcloud and MariaDB services, their environment variables, and the port mapping. This makes the deployment easier to repeat and maintain.

## Important Security Note

The passwords in this laboratory configuration are demonstration values. Real deployments should use strong credentials, protect secrets, and avoid committing production passwords to public repositories.
