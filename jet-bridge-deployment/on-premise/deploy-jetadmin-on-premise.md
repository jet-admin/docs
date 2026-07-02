---
description: Install JetAdmin On-Premise using the automated installation script
---

# Deploy JetAdmin On-Premise

## Step 1: Enable On-Premise Deployment

In your JetAdmin Cloud Instance:

1. Open Environment Settings.
2. Select **On-Premise**.
3. Set deployment type to **On-Premise**.

{% @arcade/embed flowId="hXVDSqYN2qq30CCAjXhs" url="https://app.arcade.software/share/hXVDSqYN2qq30CCAjXhs" %}

## Step 2: Run Installation Command

Copy the installation command:

```bash
sudo sh -c "$(curl -sS https://link-dev.jetadmin.io/install/...)"
```

This command downloads and executes the JetAdmin installation script, which prepares your server for the On-Premise deployment.

{% hint style="info" %}
The installation script automatically downloads the required deployment files, creates the necessary directories, and configures the JetAdmin deployment environment.
{% endhint %}

After running the command, you will be asked to confirm the installation location.

{% embed url="https://www.loom.com/share/2e07412b2a434751a4506ee6c0d20e50" %}

## Step 3: Choose Deployment Mode

When installation completes, select one of the available options.

```bash
What would you like to do next?

1. Start JetAdmin now (localhost only, http://)
2. Setup custom domain + HTTPS 
3. Exit
```

## Deployment Scenarios

Choose the deployment option that best fits your environment.

### Scenario 1: Localhost Deployment (HTTP)

Choose:

```
1. Start JetAdmin now (localhost only)
```

This option is recommended for:

* Local development
* Testing
* Proof-of-concept environments

The installer will start all required services locally.

Once deployment is complete, open:

```
http://localhost
```

or the URL displayed by the installer.

&#x20;

{% embed url="https://www.loom.com/share/9f661462bea84bb89fe976ee6479952f" %}

### Scenario 2: Production Deployment (HTTPS + Custom Domain)

Choose:

```
2. Setup custom domain + HTTPS
```

#### Select an SSL Certificate Option

Choose how JetAdmin should configure HTTPS:

```bash
1. Issue a new Let's Encrypt certificate via HTTP-01 
2. Use an existing certificate 
3. Renew an expiring Let's Encrypt certificate
```

For this guide, select: **1**

{% hint style="warning" %}
Port 80 must be publicly accessible for Let's Encrypt validation.
{% endhint %}

#### Configure Your Domain

Provide the required domain information:

```bash
Root domain: getexample.com
Admin email: user@example.com
```

The installer will then prompt for service subdomains.

Default values are pre-filled and can usually be accepted by pressing Enter.

Services include:

* Frontend
* IDE
* Backend
* Backend-N
* DataSync
* Workflows
* DataSrc
* JetBridge
* Flower

#### Create DNS Records

The installer will display the required DNS records.

A wildcard DNS record is recommended:

| Type | Host | Value          |
| ---- | ---- | -------------- |
| A    | \*   | Your Server IP |

This allows all JetAdmin services to resolve automatically.

**Note:** If your DNS provider does not support wildcard records, create individual records.

Example:

<table data-header-hidden data-search="false"><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>Type</td><td>Host</td><td>Value</td></tr><tr><td>A</td><td>app.example.com</td><td>Your Server IP</td></tr><tr><td>A</td><td>api.example.com</td><td>Your Server IP</td></tr><tr><td>A</td><td>ide.example.com</td><td>Your Server IP</td></tr><tr><td>A</td><td>data-sync.example.com</td><td>Your Server IP</td></tr><tr><td>A</td><td>workflows.example.com</td><td>Your Server IP</td></tr><tr><td>A</td><td>data.example.com</td><td>Your Server IP</td></tr><tr><td>A</td><td>jetbridge.example.com</td><td>Your Server IP</td></tr><tr><td>A</td><td>flower.example.com</td><td>Your Server IP</td></tr></tbody></table>

After creating the records, confirm the DNS configuration when prompted.

#### Access JetAdmin

After DNS validation, JetAdmin automatically completes the deployment by:

* Requesting SSL certificates
* Downloading Docker images
* Creating containers
* Starting services
* Running database migrations
* Adding a cron job to renew the Let’s Encrypt certificate

{% embed url="https://www.loom.com/share/78fa75b9892b4c8c8336823667793718" %}

### Verify Your Deployment

Once the installation is complete, open a web browser and navigate to:

* `http://localhost:80` for localhost deployments, or
* [app.example.com](http://app.example.com) for a custom domain when deploying with HTTPS.

If the JetAdmin sign-up page loads successfully, the deployment has completed successfully.

Create a new account, then create your first project and add resources to start building with JetAdmin.

{% embed url="https://www.loom.com/share/5fdf131989f74de5b68f3284884af6e9" %}
