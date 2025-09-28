---
description: >-
  Common pitfalls when using MCP servers in JetAdmin and best practices for
  reliable integrations.
---

# Limitations & Best Practices

### Limitations & Common Gotchas

While MCP servers make integration easier, there are some limitations to be aware of:

* Some MCP servers may only expose read-only actions, which restricts workflow possibilities.
* Rate limits on external APIs can prevent workflows from executing if actions are called too frequently.
* Private servers can be blocked by firewalls or network restrictions if not configured properly.
* Parameter validation is necessary: if required parameters are missing or incorrectly formatted, actions may fail.

### Best Practices

To ensure smooth and reliable use of MCP servers in JetAdmin, follow these practices:

* Always test MCP servers in a staging environment before connecting them to production apps.
* Monitor usage and error logs in JetAdmin to detect and resolve issues early.
* Rotate credentials regularly (every 60–90 days) to minimize security risks.
* Document available actions and expected parameters so team members can use them consistently.
* Start with simple workflows or component bindings to validate server behavior before building complex automations.

By following these best practices, you can safely and efficiently leverage MCP servers like the Slack MCP server from Smithery across JetAdmin apps, workflows, and AI agents.
