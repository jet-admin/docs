---
description: >-
  Below are the links and instructions for checking the health status of the
  basic service:
---

# Service Health Check

{% hint style="info" %}
**Note:** Replace placeholders such as `COMMON_BACKEND_URL`, `COMMON_BACKEND_NODE_URL`, etc., with the actual URLs specific to your environment.
{% endhint %}

* In case of any errors or unexpected responses, look at the service logs for further troubleshooting steps.
  1. **Backend Service:**
     * URL: `COMMON_BACKEND_URL/api/check_health/`
  2. **Backend Node Service:**
     * URL: `COMMON_BACKEND_NODE_URL/check_health/`
  3. **Data Sync Service:**
     * URL: `COMMON_DATA_SYNC_URL/check_health/`
  4. **Workflows Service:**
     * URL: `COMMON_WORKFLOWS_URL/check_health/`
  5. **Data Sources API:**
     * URL: `COMMON_DATA_SOURCES_API_URL/check_health/`
  6.  **Jet Bridge Cloud Service:**\
      Please note that JetBridge health check does not have a specific method. When accessing the service, it will redirect, and the output will resemble the information shown in the screenshot.

      * URL: `COMMON_JET_BRIDGE_CLOUD_URL/api/`



      <div data-full-width="true">

      <figure><img src="../../.gitbook/assets/Screenshot 2024-03-25 at 18.55.00.png" alt=""><figcaption></figcaption></figure>

      </div>

{% hint style="info" %}
URLs should be similar to the URLs in your .env file. You can access the .env file by navigating to the "jet-onpremise" directory and opening it with the Nano text editor using the following commands:

```bash
cd jet-onpremise
nano .env
```
{% endhint %}

A successful response typically indicates details (healthy true/false, version) in the response body.
