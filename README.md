# Docker Compose Netbox Deployment
A simple example with all in one docker compose based netbox deployment.

Based on the netbox docker image by [linuxserver.io](https://github.com/linuxserver/docker-netbox).

## Featuring
- [x] Postgres Database
- [x] Redis Database
- [x] Configurable access information
- [ ] Traefik with SSL and HTTPS Basic Authentication for exposure to the internet
- [x] Import script for [device-type library](https://github.com/netbox-community/devicetype-library/tree/master)

## Deploying

### Prerequisites
- Docker & Docker Compose
- (fast) internet connection to pull the docker images

### Configuration
Please adjust the values in the .env files and the .conf file to your liking before actually using it.

### Running

`docker compose up [-d]`

### Importing Device Library
- This script will import the following vendors: `APC,Brocade,Cisco,D-Link,Dell,Fortinet,Generic,HPE,Fujitsu,Intel,Lenovo,Raspberry Pi,TP-Link,Supermicro,Zyxel,IBM`
- It is using the prebuilt docker image from [netbox-community](https://github.com/netbox-community/Device-Type-Library-Import)

#### docker run command
`docker run -e "NETBOX_URL=http://<Hostname or IP>:8000/" -e "NETBOX_TOKEN=<your-netbox-token>" -e "VENDORS=APC,Brocade,Cisco,D-Link,Dell,Fortinet,Generic,HPE,Fujitsu,Intel,Lenovo,Raspberry Pi,TP-Link,Supermicro,Zyxel,IBM" ghcr.io/minitriga/netbox-device-type-library-import`

**Check the logs from the netbox container:**
`docker logs -f --tail 100 --timestamps netbox`

