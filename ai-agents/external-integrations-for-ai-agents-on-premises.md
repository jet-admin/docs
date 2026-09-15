---
description: >-
  Configure Slack and Telegram integrations for AI agents in on-premises
  deployments using environment variables.
---

# External Integrations for AI Agents (On-Premises)

In on-premises deployments, external integrations must be configured manually.

JetAdmin supports integrations that allow AI agents to interact with users through messaging platforms and enable authentication via Slack.

All integrations are optional and require adding environment variables to your deployment configuration.

## **Slack Integration (AI Agent)**

Connect AI agents to Slack to enable interaction within channels and conversations.

### **Configuration**

Add the following variables to your environment configuration:

```
#------------------------------------------------------------------------------
# Slack Integration for AI agent (on-premises)
#------------------------------------------------------------------------------
SLACK_APP_ID=
SLACK_SIGNING_SECRET=
SLACK_BOT_NAME=Example Bot
SLACK_ADD_AGENT_COMMAND=/add-agent
```

### **Parameters**

| Variable                   | Description                                              | Source                                         |
| -------------------------- | -------------------------------------------------------- | ---------------------------------------------- |
| SLACK\_APP\_ID             | Unique identifier of your Slack application              | Slack App → Basic Information → App ID         |
| SLACK\_SIGNING\_SECRET     | Verifies that incoming requests originate from Slack     | Slack App → Basic Information → Signing Secret |
| SLACK\_BOT\_NAME           | Display name of the bot in Slack                         | Defined by you                                 |
| SLACK\_ADD\_AGENT\_COMMAND | Slash command used to add the AI agent to a conversation | Slack App → Slash Commands                     |

## **Telegram Integration (AI Agent)**

Enable AI agent interaction via Telegram bots.

### **Configuration**

Add the following variables to your environment configuration:

```
#------------------------------------------------------------------------------
# Telegram Integration for AI agent (on-premises)
#------------------------------------------------------------------------------
TELEGRAM_BOT_TOKEN=
TELEGRAM_BOT_NAME=Example Bot
```

### **Parameters**

| Variable             | Description                                      | Source                  |
| -------------------- | ------------------------------------------------ | ----------------------- |
| TELEGRAM\_BOT\_TOKEN | Token used to authenticate with Telegram Bot API | Telegram → `@BotFather` |
| TELEGRAM\_BOT\_NAME  | Display name of the bot in Telegram              | Defined by you          |

## **Sign in with Slack (OAuth)**

Allow users to authenticate using their Slack accounts.

### **Configuration**

Add the following variables to your environment configuration:

```
#------------------------------------------------------------------------------
# Sign in with Slack (on-premises)
#------------------------------------------------------------------------------
SOCIAL_AUTH_BACKEND_SHARED_PARAMS_SLACK_KEY=
SOCIAL_AUTH_BACKEND_SHARED_PARAMS_SLACK_SECRET=
```

### **Parameters**

| Variable                                             | Description               | Source                                        |
| ---------------------------------------------------- | ------------------------- | --------------------------------------------- |
| SOCIAL\_AUTH\_BACKEND\_SHARED\_PARAMS\_SLACK\_KEY    | Slack OAuth Client ID     | Slack App → Basic Information → Client ID     |
| SOCIAL\_AUTH\_BACKEND\_SHARED\_PARAMS\_SLACK\_SECRET | Slack OAuth Client Secret | Slack App → Basic Information → Client Secret |

{% hint style="info" %}
#### **Important**

* In on-premises deployments, integrations do not work until configured manually
* Invalid or missing credentials will prevent functionality
* Restart the application after updating environment variables
{% endhint %}
