# Deploying WordPress with Docker

This repository contains the necessary files to deploy a WordPress site using Docker and Docker Compose.

## Prerequisites

- Docker
- Docker Compose

## File `docker-compose.yml` Description

The `docker-compose.yml` file contains configuration for two services: `wordpress` and `db`.

- The `wordpress` service uses the official WordPress image, exposes port 8080 and sets the necessary environment variables for connecting to the database. Data is persisted using a volume named `wordpress`.
- The `db` service uses the MySQL 5.7 image, sets the environment variables for the database and user creation, and persists the data using a volume named `db`.

The database credentials are pre-set in the configuration, you don't need to modify them unless you wish to.

## Usage

1. Clone this repository on your system.
```sh
git clone https://github.com/Chocapikk/projet-docker.git
```

2. Navigate into the project directory.
```sh
cd projet-docker
```

3. Run Docker Compose to start up the Docker services.
```sh
sudo docker-compose up --build -d --remove-orphans
```

After running these commands, WordPress and MySQL will be running in separate Docker containers. You can access your WordPress site by navigating to `http://localhost:8080` in your web browser.

Please note that on the first run, you will need to go through the WordPress installation process, which will ask for the username and password set in the `docker-compose.yml` file.

