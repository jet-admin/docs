---
description: >-
  Connect Stripe to Jet Admin to build billing dashboards and support tools on
  your charges, invoices and subscriptions — including refunds from inside your
  app.
---

# Stripe

Stripe is the one source on this list where the app layer usually needs to **write**, not just read: issuing a refund or cancelling a subscription from a support tool instead of the Stripe dashboard.

## What you get

Jet syncs the following Stripe objects:

* Charges
* Customers
* Disputes
* Invoices
* Plans
* Products
* Refunds

Because Jet Admin can also act on Stripe, you can build refunds and subscription cancellation directly into your app, and alert your account team to upcoming renewals, cancellations and delinquencies.

## Before you start

* A Stripe account and your **Secret API key**
* A clear decision about test versus live mode — see the warning below

{% hint style="danger" %}
**Check which key you're using.** Stripe's dashboard shows a test key by default. A test key connects to test data and nothing you build will affect real customers; a live secret key can move real money the moment you wire up a refund action. Build against test, then swap the key.
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
#### Gate the write actions

Before you ship, restrict refund and cancellation actions with [visibility rules](../../user-guide/components-visibility/) or team permissions so only the right people can trigger them.
{% endstep %}
{% endstepper %}

## Troubleshooting

**I can see test data but not real customers.** You connected a test secret key. Replace it with the live key in the resource settings.

**A refund action fails.** The key may be restricted. Confirm the secret key has write access to charges and refunds in Stripe.

**Invoice totals look wrong in a blended table.** Stripe stores amounts in the smallest currency unit — cents, not dollars. Divide in a [computed column](../../user-guide/data/computed-columns/) rather than assuming the raw value.

{% content-ref url="./" %}
[.](./)
{% endcontent-ref %}
