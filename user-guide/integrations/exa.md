---
description: >-
  Learn how to connect Exa to JetAdmin to perform AI-powered web search,
  retrieve webpage content, and provide AI Agents with up-to-date information.
---

# Exa

Exa is an AI-powered search engine designed for applications and AI systems. It enables semantic web search and content retrieval, helping AI Agents find relevant information beyond traditional keyword-based search.

## Connecting Exa

To connect your Exa account:

1. Open the **Data** tab from the left sidebar.
2. Click **Add Resource**.
3. Select **Exa** from the list of available resources.
4. Authenticate your Exa account.

{% @arcade/embed flowId="SOubhnZ6703uUEweoFkX" url="https://app.arcade.software/share/SOubhnZ6703uUEweoFkX" %}

{% hint style="info" %}
Once connected, the Exa resource becomes available anywhere JetAdmin supports Data resources.
{% endhint %}

## What can it do?

The Exa integration gives JetAdmin access to AI-powered web search and content retrieval.

From JetAdmin, you can:

* Search the web using semantic search
* Retrieve the contents of webpages
* Find relevant sources for research
* Provide AI Agents with live web information
* Use search results inside workflows and applications

## Where to use it?

Exa is most useful whenever your application needs web research, live information, or Retrieval-Augmented Generation (RAG).

You can use it in:

| JetAdmin feature   | Common use cases                                                                                          |
| ------------------ | --------------------------------------------------------------------------------------------------------- |
| **AI Agents**      | Answer questions using current web data, research topics, find reliable sources                           |
| **Workflows**      | Automate web research, collect online information, enrich business data                                   |
| **Internal tools** | Build research assistants, search portals, knowledge discovery tools, or content aggregation applications |

Typical business use cases include:

* AI-powered research
* Market and competitor analysis
* Content discovery
* Knowledge enrichment
* News monitoring
* Source retrieval for AI responses
* RAG applications

## Available tools (Actions)

| Action                    | Description                                                                     |
| ------------------------- | ------------------------------------------------------------------------------- |
| **Web Search (Advanced)** | Perform semantic web searches to find the most relevant webpages and sources.   |
| **Web Fetch**             | Retrieve and process the content of a webpage for analysis or use by AI Agents. |

> 💡 **Web Search (Advanced)** supports natural language queries, making it ideal for research tasks where keyword matching alone isn't enough.

## Example prompts for AI Agents

#### Research a topic

```
Research the latest trends in AI coding assistants and summarize the most important findings from reliable sources.
```

#### Find official documentation

```
Search for the official Stripe documentation about webhooks and summarize the implementation process.
```

#### Retrieve webpage content

```
Fetch the content from https://openai.com and summarize the latest product announcements.
```

#### Compare competitors

```
Search for the top project management platforms and compare their key features and pricing.
```

#### Find recent information

```
Search for recent news about vector databases and provide a summary with the original sources.
```

#### Enrich an AI response

```
Search the web for the latest information about the Model Context Protocol (MCP) and answer the user's question using the retrieved sources.
```

## Example

This example demonstrates how an AI Agent can use Exa to research a topic, retrieve relevant webpages, and generate an answer using live web information.

{% @arcade/embed flowId="5hzAPQ4I6g3SVgfxKKDk" url="https://app.arcade.software/share/5hzAPQ4I6g3SVgfxKKDk" %}
