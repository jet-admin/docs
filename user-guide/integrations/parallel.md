---
description: >-
  Learn how to connect Parallel to JetAdmin to perform AI-powered web search,
  retrieve webpage content, and provide AI Agents with high-quality, up-to-date
  information.
---

# Parallel

Parallel is an AI-native search platform built for large language models and AI Agents. It provides semantic web search and high-quality content extraction, making it easy to retrieve relevant information from across the web. By connecting Parallel to JetAdmin, you can search the web, fetch webpage content, and enhance AI Agents with real-time context.

## Connecting Parallel

To connect your Parallel account:

1. Open the **Data** tab from the left sidebar.
2. Click **Add Resource**.
3. Select **Parallel** from the list of available resources.
4. Authenticate your Parallel account.

{% @arcade/embed flowId="KLYRIZV9nMd2aovMhPPZ" url="https://app.arcade.software/share/KLYRIZV9nMd2aovMhPPZ" %}

{% hint style="info" %}
Once connected, the Parallel resource becomes available anywhere JetAdmin supports external resources.
{% endhint %}

## What can it do?

The Parallel integration gives JetAdmin access to AI-powered web search and webpage retrieval.

From JetAdmin, you can:

* Search the web using natural language
* Retrieve content from webpages
* Provide AI Agents with live web context
* Use search and web content inside workflows and applications

## Where to use it?

Parallel is most useful whenever your application needs **real-time web information**, **online research**, or **Retrieval-Augmented Generation (RAG)**.

You can use it in:

| JetAdmin feature   | Common use cases                                                                                                           |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------- |
| **AI Agents**      | Answer questions with current web information, perform research, retrieve reliable sources                                 |
| **Workflows**      | Automate research, enrich business data, monitor websites, or collect online information                                   |
| **Internal tools** | Build research assistants, internal search tools, competitive intelligence dashboards, or knowledge discovery applications |

Typical business use cases include:

* AI-powered research
* Market and competitor analysis
* Knowledge enrichment
* News and trend monitoring
* Source retrieval
* RAG applications

## Available tools (Actions)

| Action                 | Description                                                                                         |
| ---------------------- | --------------------------------------------------------------------------------------------------- |
| **Web Search Preview** | Search the web using natural language queries and retrieve relevant webpages and excerpts.          |
| **Web Fetch**          | Retrieve and process the content of a webpage for analysis, summarization, or AI-powered workflows. |

> Parallel is optimized for AI Agents, returning highly relevant search results and clean webpage content designed for LLMs.

## Example prompts for AI Agents

#### Research a topic

```
Research the latest trends in AI infrastructure and summarize the most important findings from reliable sources.
```

#### Find official documentation

```
Search for the official Kubernetes documentation about Ingress controllers and summarize the recommended setup.
```

#### Retrieve webpage content

```
Fetch the content from https://docs.jetadmin.io and summarize the main concepts for new users.
```

#### Compare competitors

```
Search for the top customer support platforms and compare their key features, pricing, and integrations.
```

#### Find recent information

```
Search the web for recent announcements about vector databases and summarize the latest developments.
```

#### Answer using live web data

```
Search the web for the latest information about MCP servers and answer the user's question using the retrieved sources.
```

## Example

This example demonstrates how an AI Agent can use Parallel to search the web, retrieve relevant webpages, and answer questions using live information.

{% @arcade/embed flowId="mOnFxtYpPq7GpFFLhA6o" url="https://app.arcade.software/share/mOnFxtYpPq7GpFFLhA6o" %}
