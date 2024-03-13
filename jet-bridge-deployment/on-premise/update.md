---
description: >-
  To update your Docker instance, follow these steps to upgrade to a newer
  release version
---

# Update

{% hint style="warning" %}
**Prioritize Instance Backup Before Updating:** Before proceeding with the update, it's highly advisable to back up your project. If a complete backup isn't feasible, you should consider the following:

* Generating a snapshot of your database.
* Safeguarding the environment variables stored in .env file by copying them to a secure location external to Jet Admin.
{% endhint %}

{% hint style="info" %}
**Evaluate Your Applications** \
Before rolling out the new instance, it's crucial to thoroughly test it on your most important applications, especially those that use various resources and components. Consider creating test cases, a checklist, or an internal upgrade guide to streamline this process. This document can include specific details, such as contextual information and commands, serving as a valuable resource for your team. Once the tests are successful, proceed to upgrade your production instances.
{% endhint %}

### To upgrade your deployment to a more recent version of On-premise:

Navigate to the directory where the on-premise package was previously installed.

```
cd jet-onpremise
```

Download the latest version.

```
docker-compose pull
```

{% embed url="https://www.loom.com/share/fdd927392f954805a9a0ce82d2c5ef23?sid=18a6b013-96e3-427d-85ff-61824db4aebf" %}

Restart the Jet Admin application (this process may take up to 30 seconds to minutes depending on your server). This action will restart all Jet Admin components and run them in the background.

```
docker-compose up -d
```

{% embed url="https://www.loom.com/share/9c1dc9bc867e4e83b64f149cafd708ee?sid=e4e18af9-78ad-442f-b79e-341e69818e79" %}
