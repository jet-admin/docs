---
description: >-
  Configuring the domain in the environment (.env) file is crucial for setting
  up custom domains for various services.
---

# Custom Domain Configuration on-premise

## **Steps to Replace "localhost" with Custom Domain**

**1. Navigate to the .env File:**

Use the following steps to locate and edit the .env file:

```bash
cd jet-onpremise
nano.env
```

This command will change your directory to the location where the .env file is stored and open it in the Nano text editor for editing.

#### **2. Update Common Configuration Parameters:**&#x20;

Replace occurrences of "localhost" with your custom domain in the following parameters in these parts of .env: general, system parameters, and backend node.

<pre><code>#------------------------------------------------------------------------------
# General
#------------------------------------------------------------------------------
COMMON_FRONTEND_URL=http://app.example.com
COMMON_FRONTEND_HOST=app.example.com
COMMON_BACKEND_URL=http://api.example.com
COMMON_BACKEND_HOST=api.example.com
COMMON_BACKEND_NODE_URL=http://api-node.example.com
COMMON_BACKEND_NODE_HOST=api-node.example.com
COMMON_DATA_SYNC_URL=http://data-sync.example.com
COMMON_DATA_SYNC_API_HOST=data-sync.example.com
COMMON_WORKFLOWS_URL=http://workflows.example.com
COMMON_WORKFLOWS_API_HOST=workflows.example.com
COMMON_DATA_SOURCES_API_URL=http://data.example.com
COMMON_DATA_SOURCES_API_HOST=data.example.com
COMMON_JET_BRIDGE_CLOUD_URL=http://jetbridge.example.com/api/
COMMON_JET_BRIDGE_CLOUD_HOST=jetbridge.example.com
COMMON_CENTRIFUGO_URL=ws://app.example.com:8000/connection/websocket
<strong>
</strong><strong>#------------------------------------------------------------------------------
</strong># System parameters
#------------------------------------------------------------------------------

COMMON_FLOWER_HOST=flower.example.com


#------------------------------------------------------------------------------
# Backend Node
#------------------------------------------------------------------------------

MEDIA_URL=http://api.example.com/media/
  
</code></pre>

{% hint style="warning" %}
After making changes to the .env file, restart the service by executing the following commands:

`sudo docker-compose down`&#x20;

`sudo docker-compose up -d`&#x20;

These commands will ensure that the changes take effect.
{% endhint %}

By following the above steps, you can successfully configure your custom domain in the environment file.

#### Verification:&#x20;

* After restarting the service, you can open a web browser and navigate to the URL specified in COMMON\_FRONTEND\_URL within the .env file.&#x20;
* Proceed to create a new account, then create a project, and add resources as needed.
