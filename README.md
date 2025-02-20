
# Docker Infrastructure Setup

This project involves setting up a small infrastructure using Docker Compose on a Virtual Machine. The goal is to configure and run multiple services in dedicated Docker containers with specific configurations.

## Requirements

- All configuration files should be placed in the `srcs` folder.
- A `Makefile` is required at the root of the directory to build the Docker images using `docker-compose.yml`.
- Docker images must be built from scratch (no pre-pulled images), based on either Alpine or Debian for performance.
- Containers must automatically restart in case of failure.

## Services to Set Up

- **NGINX** with TLSv1.2 or TLSv1.3 only.
- **WordPress** with php-fpm (no NGINX).
- **MariaDB** (no NGINX).
- Two **volumes**:
  - One for the WordPress database.
  - One for the WordPress website files.
- A **Docker network** to connect all containers.

## Project Setup

1. **Clone this repository** to your virtual machine.
   
   ```bash
 
