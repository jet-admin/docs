---
description: The basics of MCP servers and how they function as bridges in JetAdmin.
icon: robot
---

# MCP

Use the [MCP integration guide](./) when connecting tools and services through MCP. For ordinary data connections, start with [Data Sources](../); for custom HTTP or SQL work, use [SQL queries and API requests](../../sql-queries-and-api-requests/).

Before giving an app or agent a tool, review the endpoint, authentication, credential scope, and read or write behavior. Test with safe inputs. For agents that run through MCP clients, see [Using Agents with MCP Clients](../../../ai-agents/slack-telegram-email-and-mcp/using-agents-with-mcp-clients.md). The [Jet Admin API](/broken/pages/-M2Ezm-MS-DTMS9hxOtE) covers programmatic app access.



An **MCP (Model Context Protocol) server** is a lightweight service that exposes **tools** (functions, endpoints, or data access points) in a standardized way. JetAdmin can connect to these servers and use their tools without custom coding.

Think of it as:

```
External Service (Tool, DB, API)
        │
        ▼
     MCP Server
        │
        ▼
     JetAdmin
```

The MCP server takes care of formatting requests and responses, so JetAdmin only needs to know:

* **What operations exist** (list data, create record, update task).
* **How to call them** (parameters and auth).

This makes integrations modular, reusable, and easier to maintain.
