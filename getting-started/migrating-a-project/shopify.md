---
description: >-
  Connect a Shopify store to Jet Admin through the Admin API to build order,
  fulfilment and customer tools on your store data.
---

# Shopify

Connect Shopify through a [REST API resource](../../user-guide/data-sources/rest-api/) using the Shopify Admin API. Shopify doesn't have a native integration yet. Setup takes a few more steps than the other sources, and you can access every Admin API object.

{% hint style="warning" %}
Grant read-only scopes unless your app needs to write. A Shopify Admin API token with write scopes can modify orders and inventory.
{% endhint %}

## What you get

You can access the objects you enable in the Admin API, including:

* Products, Variants, Inventory
* Orders, Fulfilments, Transactions
* Customers
* Discounts, Price rules

{% hint style="info" %}
The REST resource uses a direct connection. It won't appear in [data blending](../../user-guide/synced-tables/) until a native Shopify integration ships.
{% endhint %}

## Before you start

* Permission to create a custom app in your Shopify admin
* The current stable Admin API version from Shopify's own documentation

## Connect Shopify

{% stepper %}
{% step %}
#### Create a custom app in Shopify

In your Shopify admin, go to **Settings → Apps and sales channels → Develop apps → Create an app**. Name it something recognisable, like `Jet Admin`.
{% endstep %}

{% step %}
#### Configure Admin API scopes

Under **Configuration → Admin API integration**, enable only what you need:

```
read_products      read_orders       read_customers
read_inventory     read_fulfillments read_discounts
```
{% endstep %}

{% step %}
#### Install the app and copy the token

Click **Install app**, then reveal and copy the **Admin API access token**. It starts with `shpat_` and is shown only once. Store it before leaving the page.
{% endstep %}

{% step %}
#### Add a REST API resource in Jet Admin

Open **Data → Add Resource → REST API** and configure:

* **Resource name**: `Shopify`
* **Base URL**: `https://your-store.myshopify.com/admin/api/<version>/`

Use the current stable API version.
{% endstep %}

{% step %}
#### Add the token as a global header

Shopify requires its own access-token header instead of Bearer auth. Add a [global header](../../user-guide/data-sources/rest-api/bearer-token.md) on the resource so every request carries it:

```
X-Shopify-Access-Token: shpat_your_token_here
```
{% endstep %}

{% step %}
#### Build your first request

In the Data Editor, create a `GET` request to `orders.json?status=any&limit=50`. Or paste Shopify's API reference into [Ask AI](../../ai-app-builder/ask-ai.md) and describe what you need. Ask AI will generate the request, handle pagination, and shape the response.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
The Admin API uses `Link` headers for pagination and applies rate limits per store. Configure pagination on the request so tables past the first 50 rows load correctly.
{% endhint %}

## Troubleshooting

Shopify returns 401. The token is in the wrong header. Shopify needs `X-Shopify-Access-Token`, not `Authorization: Bearer`. Check the global header on the resource.

Shopify returns 403 on some endpoints. The custom app is missing that scope. Add it under **Configuration → Admin API integration**, then reinstall the app.

Only 50 rows load. Pagination isn't configured. The Admin API uses `Link`-header cursors. Set pagination on the request.

Requests fail intermittently under load. You're hitting Shopify's per-store rate limit. Reduce page size or add caching on the request.

{% content-ref url="https://docs.jetadmin.io/getting-started/migrating-a-project" %}
[https://docs.jetadmin.io/getting-started/migrating-a-project](https://docs.jetadmin.io/getting-started/migrating-a-project)
{% endcontent-ref %}
