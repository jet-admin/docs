---
description: >-
  Connect HubSpot to Jet Admin with OAuth and build apps on your Contacts,
  Companies, Deals and Tickets.
---

# HubSpot

Jet Admin connects to your HubSpot portal and becomes the app layer on top of it — useful for renewal dashboards, support queues and customer portals that shouldn't expose all of HubSpot.

{% hint style="success" %}
HubSpot uses OAuth, so you authorize Jet Admin from inside HubSpot and can revoke access there at any time. There's no token to copy or rotate.
{% endhint %}

## What you get

Jet syncs the following HubSpot objects:

* Contacts
* Companies
* Deals
* Tickets

HubSpot associations become relationships in Jet Admin, so a Deal resolves to its Company.

## Before you start

* A HubSpot account that can see the objects you need — Jet Admin inherits that user's visibility
* Permission to authorize third-party apps in your HubSpot portal

## Connect HubSpot

{% stepper %}
{% step %}
#### Add HubSpot as a resource

In Jet Admin, open **Data → Add Resource** and select **HubSpot**. You can also add it while creating a new project.
{% endstep %}

{% step %}
#### Authorize access

Complete the HubSpot authorization prompt. Sign in with an account that can see everything your app needs.
{% endstep %}

{% step %}
#### Choose your connection mode

Choose **Sync** to blend HubSpot with other sources, or **Direct** for live two-way edits — editing a Deal in your app then changes it in HubSpot.
{% endstep %}

{% step %}
#### Sync the structure

Click **More → Sync Structure**. Contacts, Companies, Deals and Tickets appear in the Data Editor.
{% endstep %}

{% step %}
#### Verify associations

Confirm Deals resolve to the right Companies before building views that depend on the relationship.
{% endstep %}
{% endstepper %}

## Troubleshooting

**Some objects are missing.** Confirm the authorizing HubSpot user can see them — Jet Admin inherits that user's visibility. Only the four objects listed above are part of the standard sync.

**Authorization fails.** Your HubSpot role may not allow authorizing third-party apps. Ask a portal admin to complete the connection.

**Deals aren't linked to Companies.** The association exists in HubSpot but the structure sync predates it. Run **More → Sync Structure** again.

{% content-ref url="./" %}
[.](./)
{% endcontent-ref %}
