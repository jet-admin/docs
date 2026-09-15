---
description: >-
  JetAdmin agents can be added to Slack channels and direct messages, allowing
  users to interact with agents directly inside Slack.
---

# Using Agents in Slack

### Before You Start

Make sure you:

* Have access to the Slack workspace
* Created an agent in JetAdmin

### Setup

{% stepper %}
{% step %}
#### **Connect Slack Workspace**

Click **Connect Slack** and authorize access
{% endstep %}

{% step %}
#### Invite JetAdmin Bot

In your Slack channel, run:

```
/invite @Jet Admin
```
{% endstep %}

{% step %}
#### Connect Agent to Channel

Use the command:

```
/jet add_agent <agent_id>
```

<figure><img src="../../.gitbook/assets/image (993).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Once connected, users in the channel can interact with the agent directly.
{% endhint %}
{% endstep %}
{% endstepper %}

{% hint style="success" %}
### Supported Slack Conversations

Agents currently support:

* Public channels
* Private channels (if invited)
* Direct messages
{% endhint %}
