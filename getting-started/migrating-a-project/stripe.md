---
description: >-
  Connect Stripe to Jet Admin to build billing dashboards and support tools on
  your charges, invoices and subscriptions — including refunds from inside your
  app.
---

# Stripe

Stripe apps usually need write access to issue refunds or cancel subscriptions from a support tool instead of the Stripe dashboard.

## What you get

Jet syncs the following Stripe objects:

* Charges
* Customers
* Disputes
* Invoices
* Plans
* Products
* Refunds

Your Jet Admin app can issue Stripe refunds and cancel subscriptions. It can also alert your account team to upcoming renewals, cancellations, and delinquencies.

## Before you start

* A Stripe account and your **Secret API key**
* A decision about test or live mode. See the warning below.

{% hint style="danger" %}
Stripe's dashboard shows a test key by default. It connects to test data, so your app won't affect real customers. A live secret key can move real money as soon as you configure a refund action. Build with a test key, then switch to the live key.
{% endhint %}

## Connect Stripe

{% stepper %}
{% step %}
#### Get your Secret API key

Sign in to [Stripe](https://stripe.com/) and open your API keys. Click **Reveal** to show the secret key, then copy it.
{% endstep %}

{% step %}
#### Add Stripe as a resource

In Jet Admin, open **Data → Add Resource** and select **Stripe**. Paste the key into the **Secret Key** field.
{% endstep %}

{% step %}
#### Choose your connection mode

Choose **Sync** to blend Stripe revenue against CRM or store data. Choose **Direct** if your app issues refunds or cancels subscriptions, so those actions hit Stripe immediately.
{% endstep %}

{% step %}
#### Sync the structure

Click **More → Sync Structure**. The Stripe objects appear in the Data Editor.
{% endstep %}

{% step %}
#### Restrict write actions

Before publishing your app, restrict refund and cancellation actions with [visibility rules](../../classic-app-builder/design-and-structure/components-visibility/) or team permissions so only the right people can trigger them.
{% endstep %}
{% endstepper %}

## Troubleshooting

I can see test data but not real customers. You connected a test secret key. Replace it with the live key in the resource settings.

A refund action fails. The key may be restricted. Confirm the secret key has write access to charges and refunds in Stripe.

Invoice totals look wrong in a blended table. Stripe stores amounts in the smallest currency unit, such as cents instead of dollars. Divide the value in a [computed column](../../user-guide/data/computed-fields/) to convert it.

{% content-ref url="https://docs.jetadmin.io/getting-started/migrating-a-project" %}
[https://docs.jetadmin.io/getting-started/migrating-a-project](https://docs.jetadmin.io/getting-started/migrating-a-project)
{% endcontent-ref %}
