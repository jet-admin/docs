---
description: The basics of MCP servers and how they function as bridges in JetAdmin.
---

# MCP

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
