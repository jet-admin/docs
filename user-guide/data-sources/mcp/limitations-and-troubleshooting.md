---
description: Diagnose connection, authentication, input, and tool-result problems.
---

# MCP limitations and troubleshooting

The connected server defines the available tools, parameters, and permissions. Jet Admin cannot call an action the server does not expose.

| Symptom                          | Check                                                                   | Verify the fix                                                |
| -------------------------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------- |
| Connection times out             | Server URL, server availability, firewall, and network access           | Reconnect and load the tool list                              |
| Authentication fails             | Required authentication method, current credentials, and granted access | Run an authorized read action                                 |
| Expected tool is missing         | Server's exposed tools and account permissions                          | Confirm the tool appears for this account                     |
| Action rejects an input          | Required parameters, types, and accepted values                         | Run a known valid input                                       |
| Calls are rate-limited           | Limits from the MCP server and underlying service                       | Follow the service's retry guidance and reduce call frequency |
| Output differs from expectations | Requested record/location, response fields, units, and dates            | Compare with the same data in the external service            |
| Write action is unavailable      | Server capabilities and account permissions                             | Confirm the server exposes an authorized write operation      |

## Before using a tool in automation

[Test the tool](test-an-mcp-tool.md) with a known input. Record its expected output and whether it changes external data. Inspect tool inputs and outputs when debugging an agent or workflow.

Manage credentials according to your organization's policy and the provider's requirements. Include the action name, error, and test inputs in a support report; remove credentials from logs and screenshots.
