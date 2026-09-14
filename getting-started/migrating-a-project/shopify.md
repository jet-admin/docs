---
description: >-
  Connect a Shopify store to Jet Admin through the Admin API to build order,
  fulfilment and customer tools on your store data.
---

# Shopify

Shopify isn't a native integration yet, so you connect it as a [REST API resource](../../user-guide/integrations/rest-api/) against the Shopify Admin API. That takes a few more steps than the other sources, but it reaches every Admin API object rather than a fixed list.

{% hint style="warning" %}
Grant **read-only scopes** unless your app genuinely needs to write. A Shopify Admin API token with write scopes can modify orders and inventory.
{% endhint %}

## What you get

Whatever you enable in the Admin API, commonly:

* Products, Variants, Inventory
* Orders, Fulfilments, Transactions
* Customers
* Discounts, Price rules

{% hint style="info" %}
Because this is a REST resource, it's a **direct connection**. It won't appear in [data blending](../../user-guide/data-blending.md) until a native Shopify integration ships.
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

Click **Install app**, then reveal and copy the **Admin API access token**. It starts with `shpat_` and is shown only once — store it before you leave the page.
{% endstep %}

{% step %}
#### Add a REST API resource in Jet Admin

Open **Data → Add Resource → REST API** and configure:

* **Resource name** — `Shopify`
* **Base URL** — `https://your-store.myshopify.com/admin/api/<version>/`

Use the current stable API version rather than pinning an old one.
{% endstep %}

{% step %}
#### Add the token as a global header

Shopify doesn't use Bearer auth. Add a [global header](../../user-guide/integrations/rest-api/bearer-token.md) on the resource so every request carries it:

```
X-Shopify-Access-Token: shpat_your_token_here
```
{% endstep %}

{% step %}
#### Build your first request

In the Data Editor, create a `GET` request to `orders.json?status=any&limit=50`. Or paste Shopify's API reference into [Ask AI](../../ask-ai.md) and describe what you need — it will generate the request, handle pagination and shape the response.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
The Admin API paginates with `Link` headers rather than page numbers, and rate-limits per store. Configure pagination on the request so tables past the first 50 rows load correctly.
{% endhint %}

## Troubleshooting

**Shopify returns 401.** The token is in the wrong header. Shopify needs `X-Shopify-Access-Token`, not `Authorization: Bearer`. Check the global header on the resource.

**Shopify returns 403 on some endpoints.** The custom app is missing that scope. Add it under **Configuration → Admin API integration**, then reinstall the app.

**Only 50 rows load.** Pagination isn't configured. The Admin API uses `Link`-header cursors — set pagination on the request.

**Requests fail intermittently under load.** You're hitting Shopify's per-store rate limit. Reduce page size or add caching on the request.

{% content-ref url="./" %}
[.](./)
{% endcontent-ref %}
