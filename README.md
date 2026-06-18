# Xray Docker Server

Docker deployment of Xray proxy server on Ubuntu VPS.

## Technologies

- Linux Ubuntu
- Docker
- Xray-core
- VPS/VDS
- Networking

## Features

- Containerized deployment
- Host networking
- Automatic restart
- Lightweight infrastructure

## Docker Compose

```yaml
version: '3'

services:
  xray:
    image: teddysun/xray:latest
    network_mode: host
    cap_add:
      - NET_ADMIN
    volumes:
      - /usr/local/etc/xray/config.json:/etc/xray/config.json:ro
    restart: unless-stopped
```

## Skills Demonstrated

- Linux Administration
- Docker Management
- Network Services
- VPS Deployment
- Infrastructure Management
