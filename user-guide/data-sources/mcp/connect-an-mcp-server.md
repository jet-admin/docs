---
description: Step-by-step setup for connecting MCP servers as datasources.
---

# Connect an MCP server

### Steps to connect an MCP server in JetAdmin

1. Open **Data** in your app.
2. Add a new resource → Click Add Resource and choose MCP.
3. Fill in connection details → A popup will appear with the following fields:
   * Resource Name: Defaults to _MCP_, but you can rename it (e.g., Weather Information _MCP_).
   * Server URL: Example → `https://mcp.example.com/mcp`.
   * Protocol: Options include _Auto_, _Streamable HTTP_, and _SSE_.
   * Authentication (optional):
     * None
     * API Key
     * Basic Auth
     * OAuth 2.0
4. Click Add Resource.

{% @arcade/embed url="https://app.arcade.software/share/5hbgXqLkwNKN9LhAPkhp" flowId="5hbgXqLkwNKN9LhAPkhp" %}

Once connected, the MCP server will be available as a datasource in your app. You can now bind it to data components, workflows, or agents. For example, you might call operations like `get_current_weather_tool` to display live weather for a city, or `get_weather_forecast_tool` to show multi-day forecasts directly in your JetAdmin app.

## Verify the connection

Open the resource and check the available actions. Run [Test an MCP tool](test-an-mcp-tool.md) before connecting it to an agent or workflow. The example server URL above is a placeholder; use the endpoint supplied by your MCP provider.
