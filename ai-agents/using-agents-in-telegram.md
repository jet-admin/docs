---
description: >-
  JetAdmin agents can be connected to Telegram chats and groups using the
  JetAdmin Telegram bot.
---

# Using Agents in Telegram

### Before You Start

Make sure you:

* Have a Telegram account
* Created an agent in JetAdmin

### Setup

#### Direct Message

{% stepper %}
{% step %}
Open chat with jetadmin\_bot
{% endstep %}

{% step %}
Connect your agent using:

```
/add_agent <agent_id>
```

<figure><img src="../../.gitbook/assets/image (1000).png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
Once connected, you can chat with the agent directly in Telegram.
{% endhint %}
{% endstep %}
{% endstepper %}

#### Group Chat

{% stepper %}
{% step %}
Add jetadmin\_bot to your group
{% endstep %}

{% step %}
Connect your agent using:

```
/add_agent @jetadmin_bot <agent_id>
```

<figure><img src="../../.gitbook/assets/image (995).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
### Group Permissions

Make sure the bot has permission to:

* Read messages
* Send messages

Without these permissions, the agent may not respond correctly.
{% endhint %}
