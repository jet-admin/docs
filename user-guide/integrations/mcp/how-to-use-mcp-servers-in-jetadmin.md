---
description: Step-by-step setup for connecting MCP servers as datasources.
---

# How to Use MCP Servers in JetAdmin

### Steps to connect an MCP server in JetAdmin

1. Open the Data section → go to Data.
2. Add a new resource → Click Add Resource and choose MCP.
3. Fill in connection details → A popup will appear with the following fields:
   * Resource Name: Defaults to _MCP_, but you can rename it (e.g., Weather Information _MCP_).&#x20;
   * Server URL: Example → `https://mcp.example.com/mcp`.
   * Protocol: Options include _Auto_, _Streamable HTTP_, and _SSE_.
   * Authentication (optional):
     * None
     * API Key
     * Basic Auth
     * OAuth 2.0
4. Click Add Resource.

{% @arcade/embed flowId="5hbgXqLkwNKN9LhAPkhp" url="https://app.arcade.software/share/5hbgXqLkwNKN9LhAPkhp" %}

Once connected, the MCP server will be available as a datasource in your app. You can now bind it to data components, workflows, or agents. For example, you might call operations like `get_current_weather_tool` to display live weather for a city, or `get_weather_forecast_tool` to show multi-day forecasts directly in your JetAdmin app.
