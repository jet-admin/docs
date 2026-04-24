---
description: >-
  Agents in JetAdmin can be connected to external platforms and used as bots.
  This allows you to interact with your agents directly from tools like Slack,
  Telegram, and morewithout opening your app.
---

# Using Agents in External Tools (Slack,Telegram,...)

#### Supported Platforms

You can connect agents to:

* Slack (channels and direct messages)
* Telegram (direct messages and groups)
* Discord _(planned)_
* WhatsApp _(planned)_
* MCP clients and other tools _(planned)_

### How to Connect an Agent

To connect an agent:

1. Open your agent
2. Click **“Add to”** (top center)
3. Follow the setup instructions for your selected platform

{% @arcade/embed flowId="boxU3PyJHQFOhWw6DeUV" url="https://app.arcade.software/share/boxU3PyJHQFOhWw6DeUV" %}

### Slack Setup

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

<figure><img src="../.gitbook/assets/image (993).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

### Telegram Setup

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

<figure><img src="../.gitbook/assets/image (994).png" alt=""><figcaption></figcaption></figure>
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
/add_agent@jetadmin_bot <agent_id>
```

<figure><img src="../.gitbook/assets/image (995).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
