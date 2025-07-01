---
description: >-
  This guide should help you set up and configure Nginx, customize the server
  block to match your requirements, and update your application's .env file to
  reflect the changes.
---

# Nginx Configuration

### **Installing Nginx**

To install Nginx, you can use the apt package manager. Simply open a terminal and run the following commands:

```bash
sudo apt update
sudo apt install nginx
```

### **Navigating to the `.env` File**

Use the following steps to locate and edit the `.env` file:

```bash
cd jet-onpremise
nano .env
```

This command will change your directory to the location where the `.env` file is stored and open it in the Nano text editor for editing.

### **Updating `.env` File**

After navigating to the `.env` file, update your application's `.env` file with the appropriate domain names. Replace `localhost` with your custom domain across the relevant variables:

```dotenv
COMMON_FRONTEND_URL=https://app.example.com
COMMON_FRONTEND_HOST=app.example.com
COMMON_BACKEND_URL=https://api.example.com
COMMON_BACKEND_HOST=api.example.com
COMMON_BACKEND_NODE_URL=https://api-node.example.com
COMMON_BACKEND_NODE_HOST=api-node.example.com
COMMON_DATA_SYNC_URL=https://data-sync.example.com
COMMON_DATA_SYNC_API_HOST=data-sync.example.com
COMMON_WORKFLOWS_URL=https://workflows.example.com
COMMON_WORKFLOWS_API_HOST=workflows.example.com
COMMON_DATA_SOURCES_API_URL=https://data.example.com
COMMON_DATA_SOURCES_API_HOST=data.example.com
COMMON_JET_BRIDGE_CLOUD_URL=https://jetbridge.example.com/api/
COMMON_JET_BRIDGE_CLOUD_HOST=jetbridge.example.com
COMMON_CENTRIFUGO_URL=wss://app.example.com:8000/connection/websocket
```

{% hint style="warning" %}
**Important:**\
If you're deploying Nginx **on the same host** as `onpremise`, you must update the `NGINX_PORT` variable in the `.env` file:

```
NGINX_PORT=8080
```

By default, NGINX\_PORT is set to 80, which conflicts with the external Nginx server that also listens on port 80. Without this change, Nginx will fail to start due to a port conflict.
{% endhint %}

### **Navigating to Nginx Configuration File:**&#x20;

Use the following command to navigate to the directory where the Nginx configuration files are stored:

```bash
cd /etc/nginx/conf.d
```

### **Updating Nginx Configuration:**&#x20;

Open the Nginx configuration file in a text editor, such as Nano:

```bash
sudo nano your_configuration_file
```

### **Nginx Configuration**

Below is an example configuration for Nginx server block. This configuration handles HTTPS requests, proxying them to a jet-onpremise\_nginx running on port 8080. Adjust the paths and server names to match your setup.

```nginx
server {
    listen 80 default_server;
    server_name _; 
    return 301 https://$host$request_uri;
}

server {
    listen 443 http2 ssl;
    ssl_certificate /etc/ssl/certs/example.com/tls.crt;     # Note: Replace example.com with your domain
    ssl_certificate_key /etc/ssl/certs/example.com/tls.key; # Note: Replace example.com with your domain
    server_name app.example.com api.example.com api-node.example.com data-sync.example.com workflows.example.com data.example.com flower.example.com jetbridge.example.com, ...;  #Your server names

    client_max_body_size 32m;
    add_header 'Strict-Transport-Security' 'max-age=0;';
    merge_slashes off;
    large_client_header_buffers 4 32k;

    location / {
        proxy_hide_header 'Access-Control-Allow-Origin';
        proxy_hide_header 'Access-Control-Allow-Methods';
        proxy_hide_header 'Access-Control-Allow-Headers';
        proxy_hide_header 'Access-Control-Expose-Headers';

        add_header 'Access-Control-Allow-Origin' '*' always;
        add_header 'Access-Control-Allow-Methods' 'GET, POST, PUT, PATCH, DELETE, OPTIONS';
        add_header 'Access-Control-Allow-Headers' 'Authorization,DNT,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type,Range,X-HTTP-Method-Override,X-Bridge-Settings,X-Stick-Session';
        add_header 'Access-Control-Allow-Credentials' 'true';
        add_header 'Access-Control-Expose-Headers' 'Content-Length,Content-Range,Content-Disposition,Content-Type';
        add_header 'Strict-Transport-Security' 'max-age=0;';
        access_log off;

        proxy_pass http://127.0.0.1:8080;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header Host $host;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_buffer_size 128k;
        proxy_buffers 8 128k;
        proxy_busy_buffers_size 128k;
    }
}
```

{% hint style="warning" %}
Replace example.com with your domain
{% endhint %}

{% hint style="info" %}
To check the configuration and reload the Nginx configuration, you can use the following commands:

```
nginx -t                   # Check configuration syntax
nginx -s reload            # Reload Nginx configuration
```
{% endhint %}

### **Verification**

After updating the `.env` file, verify the changes by accessing your application through the new custom domain in a web browser. If configured correctly, your application should now be accessible via the updated domain names.

{% hint style="danger" %}
**Note:** Don't forget to replace `example.com` with your actual domain name in both the Nginx configuration and the `.env` file. Additionally, ensure that SSL certificates are correctly configured for your domain to enable secure HTTPS connections.
{% endhint %}

{% hint style="info" %}
If you would like to use certificates from "Let's Encrypt", you can refer to this documentation:

[Link](https://certbot.eff.org/instructions?ws=nginx\&os=ubuntufocal\&tab=wildcard): Let's Encrypt Certbot Instructions
{% endhint %}
