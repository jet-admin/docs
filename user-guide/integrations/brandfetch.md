---
hidden: true
---

# Brandfetch

Brandfetch is a brand asset platform that provides access to company logos, colors, fonts, images, and brand information. By connecting Brandfetch to JetAdmin, you can automatically retrieve branding assets and company details for use in AI Agents, workflows, and internal applications.

## Connecting Brandfetch

To connect your Brandfetch account:

1. Open the **Data** tab from the left sidebar.
2. Click **Add Resource**.
3. Select **Brandfetch** from the list of available resources.
4. Authenticate your Brandfetch account.

arcade

{% hint style="info" %}
Once connected, the Brandfetch resource becomes available anywhere JetAdmin supports external resources.
{% endhint %}

## What can it do?

The Brandfetch integration gives JetAdmin access to brand assets and company information.

From JetAdmin, you can:

* Search for brands
* Retrieve company logos and brand assets
* Access brand details and context
* Identify merchants from transaction data
* Use branding information inside AI Agents and workflows

## Where to use it?

Brandfetch is most useful whenever your application needs company branding, visual assets, or brand enrichment.

You can use it in:

| JetAdmin feature   | Common use cases                                                                                                  |
| ------------------ | ----------------------------------------------------------------------------------------------------------------- |
| **AI Agents**      | Identify companies, answer brand-related questions, enrich responses with company information                     |
| **Workflows**      | Automatically retrieve logos, enrich company records, identify merchants from transactions                        |
| **Internal tools** | Display company logos, build customer directories, create CRM interfaces, or enhance dashboards with brand assets |

Typical business use cases include:

* CRM enrichment
* Customer and vendor directories
* Expense and transaction categorization
* Brand verification
* Company profile enrichment
* Marketing and sales applications

## Available tools (Actions)

| Action                                 | Description                                                                           |
| -------------------------------------- | ------------------------------------------------------------------------------------- |
| **Build Logo URLs**                    | Generate URLs for a brand's available logo assets.                                    |
| **Fetch Asset as Base64**              | Retrieve a brand asset as a Base64-encoded file for use in applications or workflows. |
| **Get Brand Context**                  | Retrieve descriptive information and context about a brand.                           |
| **Get Brand Details**                  | Retrieve brand metadata, including available assets and company information.          |
| **Identify Merchant from Transaction** | Identify the merchant associated with a transaction using transaction details.        |
| **Search Brands**                      | Search for brands by company name or domain.                                          |

## Example prompts for AI Agents

#### Find a company's branding

```
Search for Stripe using Brandfetch and return its logo, brand colors, and company information.
```

#### Retrieve a logo

```
Get the logo for Notion and provide the highest-quality version available.
```

#### Enrich a company profile

```
Retrieve the brand details for github.com and summarize the available company and branding information.
```

#### Identify a merchant

```
Identify the merchant from this transaction description: 'SQ *FIGMA SAN FRANCISCO CA' and provide the company details.
```

#### Generate logo URLs

```
Build the available logo URLs for OpenAI so I can display them in my application.
```

#### Retrieve a brand asset

```
Fetch the primary logo as a Base64 asset for Canva so it can be embedded directly into a generated document.
```

## Example

This example demonstrates how an AI Agent can search for a company, retrieve its branding assets, and use the information to enrich a CRM record.

