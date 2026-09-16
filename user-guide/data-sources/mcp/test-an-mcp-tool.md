# Test an MCP tool

Test a connected tool with known inputs before using its output in an app, workflow, or agent.

## Before you start

[Connect an MCP server](connect-an-mcp-server.md). Check the actions exposed by that server and the required parameters. Names and available operations depend on the server.

## Test the tool

1. Open the connected MCP resource and select an available action.
2. Review the action description and required inputs.
3. Enter a simple test value. For a weather action, this might be a city such as `Berlin`.
4. Run the action and inspect its response.
5. Repeat with another input to confirm the output changes as expected.

## Verify

Check that the response refers to the requested input and includes the fields your app needs. Check units and dates for weather data. A successful connection alone does not establish that every action is authorized.

## Troubleshooting

Missing actions can indicate the wrong server URL or limited authorization. Failed actions can result from missing inputs, expired credentials, rate limits, or a server error.

See the [weather example](using-mcp-server-tools-in-jetadmin-with-weather-mcp-via-smithery.md) and [MCP limitations](limitations-and-troubleshooting.md).
