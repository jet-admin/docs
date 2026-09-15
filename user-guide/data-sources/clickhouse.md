---
description: >-
  This guide explains how to connect your ClickHouse database to Jet Admin in a
  few simple steps.
---

# ClickHouse

Before you begin, ensure you have:

* Access to a running instance of ClickHouse DB.
* Connection credentials: **Host**, **Port**, **Username**, **Password**, and the specific **Database Name**.

## Steps to Connect ClickHouse DB

1. **Log in to Jet Admin**: Open Jet Admin and navigate to your application.
2. **Add a New Resource**: In the left-side menu, go to the **Data** section and click **Add Resource**.
3. **Select ClickHouse DB**: From the list of data sources, choose **ClickHouse DB**.
4. **Provide Connection Details**: Enter the required credentials, including the Host, Port, Username, Password, and Database Name.&#x20;
5. **Test the Connection**: Click **Test Connection** to ensure Jet Admin can successfully connect to your ClickHouse database.
6. **Select Tables**: Once the connection is established, choose the tables you want to use in Jet Admin.

{% @arcade/embed flowId="DwGTnOClvIRVhPVtMg3B" url="https://app.arcade.software/share/DwGTnOClvIRVhPVtMg3B" %}

{% hint style="info" %}
**Troubleshooting Tips**

1. **Connection Issues**: Double-check the credentials and ensure your ClickHouse instance is accessible.
2. **Firewall Rules**: If your ClickHouse DB is hosted in a secure environment, confirm that Jet Admin's IP addresses are whitelisted.
3. **SSL/TLS**: If your database requires encrypted connections, ensure SSL/TLS settings are correctly configured in ClickHouse and Jet Admin.
4. **Port Issues**: For ClickHouse, you need the **native connection type**. The default port for the native protocol with SSL/TLS is **9440**.&#x20;
   * Make sure to use **native protocol SSL/TLS port**.
   * Refer to ClickHouse documentation for more details: [ClickHouse Network Ports](https://clickhouse.com/docs/en/guides/sre/network-ports).
{% endhint %}
