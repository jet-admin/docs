---
description: >-
  How to connect a Slack MCP server hosted in Smithery to JetAdmin, explore its
  actions, and use them in components, workflows, or AI agents.
---

# Using MCP Server Tools in JetAdmin (with Slack MCP via Smithery)

### Overview

Once connected, an MCP server appears in JetAdmin as a datasource. JetAdmin automatically fetches all the available actions exposed by the server URL. Each action can then be configured with the required parameters and used directly within your apps. You can run these actions manually, bind their outputs to UI components, or include them in workflows and AI agents for automation.

### Using MCP Server Actions

After adding the MCP server, JetAdmin will list all **available actions**. To use an action, you select it, provide any required parameters, and choose how the result should be handled. For example, you can:

* **Bind action results to components:** Display the output of a `getChannels` action in a table or use a `sendMessage` action to trigger updates when a user interacts with a form.
* **Include in workflows:** Trigger actions as part of automated flows, e.g., when a new order is created, call an MCP action to update a Slack channel or database record.
* **Invoke in agents:** Let AI agents execute MCP actions dynamically based on user queries or system events.

This approach allows you to fully leverage the functionality exposed by the MCP server without writing custom integrations.

### Example – Slack MCP Server in Smithery

Smithery provides pre-configured MCP servers, including a Slack MCP server with multiple ready-to-use actions.

#### Step 1: Get the Server URL from Smithery

Locate the Slack MCP server in Smithery and copy its server URL. Note any required parameters for the actions you plan to use (e.g., channel ID, message text).

#### Step 2: Connect to JetAdmin

In JetAdmin, go to **Data > Add Resource > MCP**, then fill in the connection form:

* **Resource Name:** Slack MCP (or another descriptive name).
* **Server URL:** Paste the Smithery Slack MCP server URL.
* **Protocol:** Auto
* **Authentication:** Configure if required (API key, OAuth 2.0, or none).

Click **Add Resource** to complete the connection. JetAdmin will fetch all available Slack actions from the MCP server.

#### Step 3: Use Actions

Once connected, all pre-defined Slack actions are available. You can select an action, provide the required parameters, and:

* Bind the results to a table, form, or chart.
* Include the action in automated workflows.
* Let AI agents call the action dynamically.

**Example Use Case:**

* Display Slack channels in a JetAdmin table using the `getChannels` action.
* Send a message to a selected channel through a form with the `sendMessage` action.
* Trigger notifications automatically in workflows when certain events occur.

Using Smithery’s Slack MCP server, you can immediately integrate Slack actions into JetAdmin apps, workflows, and AI agents for fast, code-free internal tool development.

