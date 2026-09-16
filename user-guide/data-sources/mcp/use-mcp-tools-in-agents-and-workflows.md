# Use MCP tools in agents and workflows

Use a connected MCP action after confirming it works with a manual test.

## Before you start

Connect the server and test the action with known inputs. Note its required parameters, response fields, and whether it changes external data.

## In a workflow

1. Select an action from the connected MCP resource.
2. Supply its required inputs from the workflow's available values.
3. Run a test and inspect the action output.
4. Use the returned fields in the following step.

For workflow setup, follow [Workflow overview](https://docs.jetadmin.io/workflow/overview).

## In an agent

Make the connected resource's tools available in the agent's configuration. Describe when the agent should use the tool and what information it needs from the user. Test a specific request, then inspect the tool inputs and returned result.

For example, ask a weather agent for a forecast for a named city and date. Verify that it used those values rather than substituting a different location.

## Verify

Check the tool call as well as the final answer. Confirm that downstream steps use the intended response fields.

To connect an existing Jet Admin agent to an external MCP client, follow [Using Agents with MCP Clients](../../../ai-agents/slack-telegram-email-and-mcp/using-agents-with-mcp-clients.md). That is a different setup from adding an external MCP server as a resource.
