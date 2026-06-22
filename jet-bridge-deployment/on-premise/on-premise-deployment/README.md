---
description: Learn how to deploy an instance of On-Premise Jet Admin using Docker-compose.
hidden: true
---

# On-Premise Deployment

This deployment method grants you access to the full suite of Jet Admin services, empowering your workflow with comprehensive functionality.

## Requirements

* Command-line experience
* Experience with and setups involving Docker Engine and Docker Compose are required.

### Server Requirements

* Ubuntu 22.04 LTS (recommended)
* Minimum 4 CPU
* Minimum 8 GB RAM
* 50 GB available storage
* Public IPv4 address

### Domain Requirements

Before starting deployment:

* Own a domain name
* Be able to create DNS records
* Access to your DNS provider

Examples:

* Cloudflare
* Namecheap
* GoDaddy
* Route53

### Required Software

Install Docker:

```bash
sh <(curl -s https://get.docker.com)
```

Install Docker Compose:

```bash

sudo curl -L https://github.com/docker/compose/releases/latest/download/docker-compose-Linux-x86_64 -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

Install Nginx:

```bash
sudo apt install nginx -y
```

### Required Open Ports

```bash
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
```

Required ports:

| Port | Purpose                  |
| ---- | ------------------------ |
| 80   | Let's Encrypt validation |
| 443  | HTTPS access             |

### Verification

```bash
docker --version
docker-compose --version
nginx -v
```
