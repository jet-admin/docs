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

### <mark style="color:$danger;">step 1 and step 2 video</mark>

## Step 3: Choose Deployment Mode

When installation completes, select one of the available options.

```bash
What would you like to do next?

1. Start JetAdmin now (localhost only, http://)
2. Setup custom domain + HTTPS 
3. Exit
```

For production deployments, choose: **2**

<figure><img src="../../../.gitbook/assets/image (1011).png" alt=""><figcaption></figcaption></figure>

## Step 4: Select an SSL Certificate Option

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

<figure><img src="../../../.gitbook/assets/image (1012).png" alt=""><figcaption></figcaption></figure>

## Step 5: Configure Your Domain

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

## Step 6: Create DNS Records

The installer will display the required DNS records.

A wildcard DNS record is recommended:

| Type | Host | Value          |
| ---- | ---- | -------------- |
| A    | \*   | Your Server IP |

This allows all JetAdmin services to resolve automatically.

{% hint style="info" %}
If your DNS provider does not support wildcard records, create the individual DNS records displayed by the installer.
{% endhint %}

After creating the records, confirm the DNS configuration when prompted.

## Step 7: Access JetAdmin

After DNS validation, JetAdmin automatically completes the deployment by:

* Requesting SSL certificates
* Downloading Docker images
* Creating containers
* Starting services
* Running database migrations

{% hint style="success" %}
Installation time depends on your server resources and internet connection.

Once deployment is complete, the **URL** will be displayed in the terminal.

Open the URL in your browser and create your first user account to start using JetAdmin.
{% endhint %}

<mark style="color:$danger;">Video about success and opening in new browser tab. or one video with whole steps?</mark>

