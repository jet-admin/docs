---
description: >-
  This guide will help you connect your Databricks database to Jet Admin
  seamlessly.
---

# Databricks

Before starting, ensure you have:

* Access to a Databricks workspace.
* A Databricks cluster running and accessible.
* Connection credentials:
  * **Host**: The URL of your Databricks instance.
  * **HTTP Path**: The unique HTTP Path for your Databricks SQL endpoint.
  * **Personal Access Token (PAT)**: A token generated in your Databricks account.

### Steps to Connect Databricks DB to Jet Admin

1. **Log in to Jet Admin**: Open Jet Admin and navigate to your application.
2. **Add a New Resource**: In the left-side menu, go to the **Data** section and click **Add Resource**.
3. **Select Databricks DB**: From the list of data sources, choose **Databricks DB**.
4. **Provide Connection Details**:
   * Enter the **Host** URL of your Databricks instance.
   * Input the **HTTP Path** from your Databricks SQL endpoint.
   * Add the **Personal Access Token** (PAT) generated in Databricks.
5. **Test the Connection**: Click **Test Connection** to verify that Jet Admin can successfully connect to your Databricks database.
6. **Select Tables**: Once the connection is verified, choose the tables you want to access in Jet Admin.

{% @arcade/embed flowId="nyKyR3ZQ9e9hRCA3v7Er" url="https://app.arcade.software/share/nyKyR3ZQ9e9hRCA3v7Er" %}

### How to Generate a Personal Access Token (PAT) in Databricks

1. Log in to your Databricks account.
2. Navigate to your **User Settings**.
3. Under the **Access Tokens** section, click **Generate New Token**.
4. Specify a token name and expiration date, then generate the token.

{% hint style="info" %}
**Troubleshooting Tips**

* **Connection Issues**: Double-check your Host, HTTP Path, and PAT for accuracy.
* **Cluster Status**: Ensure your Databricks cluster is running and accessible.
* **Firewall Settings**: If your Databricks is in a secure environment, confirm that Jet Admin’s IP addresses are whitelisted.
{% endhint %}
