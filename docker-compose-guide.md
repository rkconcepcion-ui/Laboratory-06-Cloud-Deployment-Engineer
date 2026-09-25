# Docker Compose Guide

## What does the `services:` block do?

The `services:` block defines the containers that make up the application. In this project, it contains two services: `database` for MariaDB and `app` for Nextcloud. Docker Compose uses these definitions to create and run the required containers.

## How does the Nextcloud app find the database?

The Nextcloud app uses the `MYSQL_HOST` environment variable to identify the database service. In the Compose file, it is set to `database`, which matches the name of the MariaDB service:

```yaml
- MYSQL_HOST=database
```

Docker Compose creates a network for the services, allowing the Nextcloud container to communicate with the MariaDB container using the service name `database`.

## Difference Between `docker run` and `docker-compose up -d`

`docker run` is normally used to create and start an individual container using command-line options. For example, it can be used to start a single Nginx container.

`docker-compose up -d` is used to deploy multiple related containers defined in a Compose YAML file. In this mission, one command starts both the Nextcloud application and MariaDB database. The `-d` option runs the containers in detached mode, allowing the terminal to be used for other commands.

## Infrastructure as Code

Docker Compose demonstrates Infrastructure as Code because the application infrastructure is described in a YAML configuration file. Instead of manually entering many commands, the configuration can be reused to consistently deploy the same multi-container environment.

