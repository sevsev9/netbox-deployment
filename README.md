# Docker Compose Netbox Deployment
A simple example with all in one docker compose based netbox deployment.

Based on the netbox docker image by [linuxserver.io](https://github.com/linuxserver/docker-netbox).

## Featuring
- [x] Postgres Database
- [x] Redis Database
- [x] Configurable access information
- [ ] Traefik with SSL and HTTPS Basic Authentication for exposure to the internet

## Deploying

### Prerequisites
- Docker & Docker Compose
- (fast) internet connection to pull the docker images

### Configuration
Please adjust the values in the .env files and the .conf file to your liking before actually using it.

### Running

`docker compose up [-d]`
