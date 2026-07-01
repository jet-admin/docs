---
description: >-
  Verify your server, operating system, network, and software requirements
  before deploying JetAdmin On-Premise.
---

# Prerequisites

Review and complete the following requirements before starting the JetAdmin On-Premise installation.

## Requirements

* Command-line experience
* Experience with and setups involving Docker Engine and Docker Compose are required.

#### Supported Operating Systems

JetAdmin On-Premise supports the following operating systems:

* Ubuntu 22.04+
* Debian 13+
* CentOS Stream 9+
* RHEL 10+

### Server Requirements

* Minimum 4 CPU
* Minimum 8 GB RAM
* 50 GB available storage
* Public IP address (required for HTTPS deployments)

#### Connect to Your Server

Before running the installation commands, connect to your server using SSH.

Example:

```bash
ssh username@your-server-ip
```

If you are running JetAdmin on your local machine, open a terminal application and run the commands locally.

#### Domain Requirements (HTTPS Deployments Only)

If you plan to deploy JetAdmin with HTTPS:

* Own a domain name
* Have access to your DNS provider
* Be able to create DNS records

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

<div align="left"><figure><img src="../../.gitbook/assets/image (1013).png" alt=""><figcaption></figcaption></figure></div>
