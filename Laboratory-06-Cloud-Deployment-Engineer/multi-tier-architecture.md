# Multi-Tier Architecture

## What Is a Two-Tier Architecture?

A two-tier architecture is an application design that separates the web application from the database. In this project, Nextcloud is the web application, while MariaDB is the database. Both work together to provide a private cloud storage system.

## The Web/Application Tier

The web/application tier is responsible for displaying the user interface and handling requests from users. In this project, the Nextcloud container allows users to access the private cloud storage website through a web browser. It listens on port 80 inside the container, which is mapped to port 8080 in the playground.

## The Database Tier

The database tier stores persistent information needed by the application, such as user accounts and file metadata. In this project, MariaDB stores Nextcloud's database information. The database runs in a separate container from the Nextcloud application.

## Why Separate Them?

Separating the web application and database into different containers makes the system easier to manage and maintain. Each container has its own responsibility, so the application and database can be updated or configured separately. Docker Compose also helps deploy and manage both services using one configuration file.
