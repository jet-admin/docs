---
description: >-
  The differences between public and private MCP servers, and how tools like
  Waystation and Smithery help manage them.
---

# Public vs Private MCP Servers

### Overview

MCP servers generally fall into two categories: public and private. Public MCP servers are hosted by third parties and are often preconfigured for common APIs, making them easy to set up and quick to integrate for example, a GitHub MCP server for accessing repository data. Private MCP servers, on the other hand, run inside your own environment, such as Docker, Kubernetes, or a VM. While they require more setup and maintenance, they give you full control over access policies and security, which makes them especially suitable for handling sensitive or production-level data.

### Comparison

| Aspect          | Public MCP Server     | Private MCP Server    |
| --------------- | --------------------- | --------------------- |
| Setup           | Ready to use          | You manage deployment |
| Security        | Shared / less control | Full control          |
| Customizability | Limited               | Highly customizable   |

{% hint style="info" %}
#### Helpful Tools

* [**Waystation**](https://github.com/waystationai/waystation)**:** Discover, test, and manage MCP servers.
* [**Smithery**](https://smithery.ai/)**:** Browse and publish MCP servers with hosting options.

Both platforms support different authentication methods like API keys, OAuth, or environment variables.
{% endhint %}
