---
description: >-
  Learn how to connect Apify to JetAdmin to run Actors, retrieve web data, and
  use Apify tools in AI Agents and workflows.
---

# Apify

Apify is a web automation and data extraction platform that lets you run pre-built or custom **Actors** to collect data from websites, automate browser tasks, and process large amounts of online information.

{% hint style="info" %}
**What is an Actor?**

An **Actor** is an executable application on Apify that performs a specific task, such as scraping a website, crawling pages, extracting structured information, or automating browser actions. Thousands of ready-made Actors are available in the Apify Store, or you can create your own.
{% endhint %}

## Connecting Apify

To connect your Apify account:

1. Navigate to the **Data** tab from the left sidebar.
2. Click **Add Resource**.
3. Select **Apify** from the list of available resources.
4. Authenticate your Apify account.

{% @arcade/embed flowId="cIWtddJQuVpyDzZDuJeE" url="https://app.arcade.software/share/cIWtddJQuVpyDzZDuJeE" %}

> ℹ️ Once connected, all available Apify tools can be used inside AI Agents, Workflows, and other JetAdmin features that support resources.

### What can it do?

The Apify integration gives JetAdmin access to your Apify account and its Actors.

From JetAdmin, you can:

* Run Apify Actors
* Monitor and manage Actor runs
* Retrieve datasets and stored records
* Search Actors and Apify documentation
* Use Apify tools inside AI Agents and workflows

### Where to use it?

Apify is most useful whenever your application needs live data from the web or web automation.

You can use it in:

| JetAdmin feature   | Common use cases                                                                                             |
| ------------------ | ------------------------------------------------------------------------------------------------------------ |
| **AI Agents**      | Research websites, answer questions using live web data, scrape information on demand                        |
| **Workflows**      | Automate data collection, monitor websites, enrich records, or trigger recurring scraping jobs               |
| **Internal tools** | Display scraped datasets, product information, business listings, or other web data inside your applications |

**Typical business use cases include:**

* Lead generation
* Competitor and market research
* Price monitoring
* Google Maps data collection
* Website content extraction
* AI knowledge enrichment

## Available tools (Actions)

| Action                         | Description                                                          |
| ------------------------------ | -------------------------------------------------------------------- |
| **Abort Actor run**            | Stops a running Actor execution.                                     |
| **Apify/rag-web-browser**      | Retrieves website content optimized for AI Agents and RAG workflows. |
| **Call Actor**                 | Starts an Actor with optional input parameters.                      |
| **Fetch Actor details**        | Returns information about a specific Actor.                          |
| **Fetch Apify docs**           | Retrieves content from the Apify documentation.                      |
| **Get Actor run**              | Returns the status and details of an Actor run.                      |
| **Get dataset items**          | Retrieves data produced by an Actor.                                 |
| **Get key-value store record** | Reads records stored in an Apify Key-Value Store.                    |
| **Search Actors**              | Searches the Apify Actor Store.                                      |
| **Search Apify docs**          | Searches the Apify documentation.                                    |

## Example prompts for AI Agents

#### Scrape a website

```
Run an Apify website crawler for https://example.com and summarize the key information.
```

#### Collect Google Maps businesses

```
Find coffee shops in Berlin using an Apify Google Maps Actor and return the business name, address, phone number, and rating.
```

#### Monitor competitor prices

```
Run my competitor price monitoring Actor and compare today's prices with the latest dataset.
```

#### Research a company

```
Find an Apify Actor that can collect company information for OpenAI, run it, and summarize the results.
```

#### Read Actor results

```
Retrieve the latest dataset from my Product Scraper Actor and create a table with product name, price, and availability.
```

#### Search Apify documentation

```
Search the Apify documentation for how to pass input parameters to an Actor and explain the process.
```

### Example

This example demonstrates how to use an AI Agent to scrape a website with Apify and summarize the results.

{% @arcade/embed flowId="GaEgu84pDGyC7f2uU9oH" url="https://app.arcade.software/share/GaEgu84pDGyC7f2uU9oH" %}
