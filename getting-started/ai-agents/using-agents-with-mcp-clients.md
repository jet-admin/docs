---
description: >-
  JetAdmin agents can be added to AI tools and MCP-compatible clients using the
  Add to AI feature.
---

# Using Agents with MCP Clients

Once enabled, your agent can be accessed directly from supported AI clients and used outside of JetAdmin.

This allows users to interact with agents from their preferred AI tools while keeping the agent configuration and logic managed inside JetAdmin.

### Using Agents with Claude AI

JetAdmin agents can be connected to Claude AI using MCP connectors. Once connected, Claude can communicate directly with your JetAdmin agent during conversations. Claude sends requests to the agent, receives responses, and displays the results directly inside the chat.

### Before You Start

Make sure you:

* Created an agent in JetAdmin
* Have access to edit the agent settings
* Have access to Claude AI connectors

### Setup in JetAdmin

{% stepper %}
{% step %}
Open your agent
{% endstep %}

{% step %}
Click **Add to** (Select Add to AI (MCP))

<figure><img src="../../.gitbook/assets/image (1003).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Click **Enable and Copy** the generated MCP URL

After enabling MCP access, JetAdmin generates a unique connector URL for the agent.

Example:

```
https://api-node.jetadmin.io/agents/mcp/abcd
```

<figure><img src="../../.gitbook/assets/image (1004).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

### Setup in Claude AI

{% stepper %}
{% step %}
Open Claude AI and go to **Connectors**

<figure><img src="../../.gitbook/assets/image (1005).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Click **Add Connector**, paste the MCP URL from JetAdmin, enter a name for the connection, and save the connector.

{% @arcade/embed flowId="95zwQooiWzP2scYAppPk" url="https://app.arcade.software/share/95zwQooiWzP2scYAppPk" %}


{% endstep %}
{% endstepper %}

> **How Claude AI Uses Your Agent**
>
> When a user sends a message in Claude, Claude checks the connected MCP connector and forwards the request to the JetAdmin agent.
>
> The agent processes the request, generates a response, and sends the result back to Claude, where it is displayed directly in the conversation.
>
> This allows users to interact with JetAdmin agents naturally through Claude AI chats.

### Example Use Cases

| Use Case                                | Description                                                                            |
| --------------------------------------- | -------------------------------------------------------------------------------------- |
| Access JetAdmin Agents from MCP Clients | Use JetAdmin agents directly inside MCP-compatible applications                        |
| Internal Knowledge Agents               | Allow MCP clients to access company knowledge through JetAdmin agents                  |
| Workflow Automation                     | Trigger JetAdmin agent workflows from MCP tools and conversations                      |
| Customer Support Agents                 | Use JetAdmin support agents inside MCP-compatible clients                              |
| Business Data Access                    | Let JetAdmin agents retrieve and process connected business data                       |
| Research and Analysis                   | Use JetAdmin agents for research, summaries, and operational tasks through MCP clients |
