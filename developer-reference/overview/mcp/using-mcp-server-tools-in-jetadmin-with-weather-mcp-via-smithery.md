---
description: >-
  How to connect a Weather MCP server hosted in Smithery to JetAdmin, explore
  its actions, and use them in components, workflows, or AI agents.
---

# Using MCP Server Tools in JetAdmin (with Weather MCP via Smithery)

### Overview

Once connected, an MCP server appears in JetAdmin as a datasource. JetAdmin automatically fetches all the available actions exposed by the server URL. Each action can then be configured with the required parameters and used directly within your apps. You can run these actions manually, bind their outputs to UI components, or include them in workflows and AI agents for automation.

### Using MCP Server Actions

After adding the Weather MCP server, JetAdmin will list all available actions. To use an action, you select it, provide any required parameters, and choose how the result should be handled. For example, you can:

* **Bind action results to components:** Display the output of a `get_current_weather_tool` action in a table, card, or chart to show live weather data for a city.
* **Include in workflows:** Trigger actions as part of automated flows, e.g., when a user selects a location, fetch a 3-day forecast automatically.
* **Invoke in agents:** Let AI agents execute MCP weather actions dynamically based on user queries (e.g., “What’s the weather in Berlin tomorrow?”).

This approach allows you to fully leverage the functionality exposed by the Weather MCP server without writing custom integrations.

### Example – Weather MCP Server in Smithery

Smithery provides pre-configured MCP servers, including a Weather MCP server with multiple ready-to-use actions.

#### Step 1: Get the Server URL from Smithery

Locate the Weather MCP server in Smithery and copy its server URL. Example:

```url
https://server.smithery.ai/@HarunGuclu/weather_mcp/mcp?api_key=yourAPIkey&profile=correct-sawfish-1eI5lV
```

{% hint style="info" %}
Take note of the available actions and their required parameters:

* **get\_current\_weather\_tool** → Get current weather info for a specific city. (Requires: `city`)
* **get\_weather\_forecast\_tool** → Get forecast for 1–10 days. (Requires: `city`, optional `days`)
* **search\_locations\_tool** → Search by city/location name. (Requires: `query`)
* **get\_live\_temp** → Legacy, current temperature only.
{% endhint %}

#### Step 2: Connect to JetAdmin

In JetAdmin, go to **Data > Add Resource > MCP**, then fill in the connection form:

* **Resource Name:** Weather MCP (or another descriptive name)
* **Server URL:** Paste the Weather MCP server URL above
* **Protocol:** Auto
* **Authentication:** API key included in the URL (no extra config needed)

Click **Add Resource** to complete the connection. JetAdmin will fetch all available Weather actions from the MCP server.

#### Step 3: Use Actions

Once connected, all pre-defined Weather actions are available. You can select an action, provide the required parameters, and:

* **Bind results to components** → Show current weather for Berlin in a JetAdmin card using `get_current_weather_tool`.
* **Include in workflows** → Fetch a 5-day forecast automatically when a user selects a city.
* **Invoke in agents** → Let AI agents answer weather-related questions dynamically.

{% @arcade/embed flowId="UItugWvK5OPGi4DgAN1z" url="https://app.arcade.software/share/UItugWvK5OPGi4DgAN1z" %}

By connecting Smithery’s Weather MCP server, you can instantly integrate live and forecasted weather data into JetAdmin apps, workflows, and AI agents for fast, code-free development.
