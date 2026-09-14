---
description: >-
  Create your first Jet Admin app, connect data, build with AI, configure
  access, and test before sharing.
icon: cube
---

# Create an app

Build an internal tool or customer portal on your existing business data. This guide takes you from a new project to a working interface, with AI assistance for components and logic, optional agents, and checks before sharing.

## Before you start

Decide who will use the app, what data they need, and which actions they should be able to perform. Start with one task, such as viewing customers and updating a customer record.

You need a Jet Admin account and access to your chosen data source. If you're experimenting without an existing database, use Jet Tables and sample data.

## 1. Create a project

Sign in to [Jet Admin](https://app.jetadmin.io/projects/create) and create a new project. Connect your data during setup, or add a resource afterward from **Data → Add Resource**.

For a worked example, follow the [internal tool quickstart](https://docs.jetadmin.io/getting-started/quickstart). For external users, follow the [customer portal guide](https://docs.jetadmin.io/getting-started/creating-a-customer-portal).

## 2. Choose where your data lives

| Starting point                                    | Use                                                                                                                                                     |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| New tables or imported files                      | [Jet Tables](https://docs.jetadmin.io/user-guide/integrations/jet-tables), the built-in PostgreSQL database with a spreadsheet-style interface          |
| An existing database                              | A connection from [Data Sources](https://docs.jetadmin.io/user-guide/integrations)                                                                      |
| Airtable, Salesforce, HubSpot, Stripe, or Shopify | The relevant [migration guide](https://docs.jetadmin.io/getting-started/migrating-a-project)                                                            |
| A service with an API                             | A [REST API](https://docs.jetadmin.io/user-guide/integrations/rest-api) or [GraphQL](https://docs.jetadmin.io/user-guide/integrations/graphql) resource |

Jet Tables supports importing CSV, XLS, XLSX, and JSON files. To try a CRM with sample Companies and Deals tables, follow [Connect your data](https://docs.jetadmin.io/getting-started/quickstart/connect-your-data).

Where an integration offers both modes, choose Direct for live reads and writes against the source. Choose Sync to mirror data into Jet Tables. Check the [connection limits](https://docs.jetadmin.io/getting-started/migrating-a-project#connection-limits) before blending sources: blended tables are read-only.

## 3. Build the first screen

Add [interface components](https://docs.jetadmin.io/user-guide/design-and-structure/components) and connect them to your data. For a first CRM screen, show customers in a table and add a detail view or form for the selected record.

Use [AI custom components](https://docs.jetadmin.io/ai-custom-components) when you need an interface beyond the standard components. Describe the data, interactions, and appearance you want, then refine the generated result.

Example component prompt:

> Create a customer summary card showing name, company, status, and account owner. Add an action to open the customer's detail view. Use a compact layout with clear field labels.

Review the generated parameters and actions, and connect them to the appropriate data and app actions.

## 4. Add logic with AI

[Ask AI](https://docs.jetadmin.io/ask-ai) can generate SQL queries, API requests, and transformation scripts.

For example, describe a query using your actual table and field names:

> Return customers whose status is Active. Include name, company, and account owner, sorted by company.

To generate a [workflow](https://docs.jetadmin.io/user-guide/workflow/workflows-with-ai), choose a trigger, open the workflow builder, and click **Ask AI**. Describe the steps, then review and customize the generated workflow.

Example workflow prompt:

> When a customer is created, send a welcome email to the customer's email address.

Check the data source, conditions, and inputs before running generated logic. Test write actions using test data and credentials.

## 5. Build an AI agent if the app needs one

[Create an agent](https://docs.jetadmin.io/agents/add-an-agent) from scratch or start with a built-in template. Agents suit tasks that depend on reasoning or context, including answering questions from connected data and coordinating actions across tools.

Define its [instructions](https://docs.jetadmin.io/agents/agent-instructions) and enable the [tools](https://docs.jetadmin.io/agents/agent-tools) needed for the task. Add an Agent Chat component to your page, or run the agent through a workflow trigger.

## 6. Configure access and test

Set up [sign-in](https://docs.jetadmin.io/user-guide/security-and-privacy/sign-in-sign-up) and [team and page permissions](https://docs.jetadmin.io/user-guide/security-and-privacy/create-and-manage-a-team). Define who can view pages, edit records, and manage the app.

Click **Preview** at the top of the builder and test the app's main task. Check:

* Records and fields load correctly.
* Forms and actions update the intended records.
* Users have the intended page and record access.
* Generated queries, workflows, and agent tools behave as expected.
* The layout works on the devices your users need.

Use a separate browser session with a test user to check sign-in and access. If you use [environments](https://docs.jetadmin.io/user-guide/project-settings/environments), verify their resource and credential configuration before testing.

## 7. Publish and share

After testing, follow [Publish your app](https://docs.jetadmin.io/getting-started/quickstart/publish-your-app) and [Sharing your app](https://docs.jetadmin.io/user-guide/core-concept/sharing-your-app).

Without app versioning, changes to the working version are immediately visible to users. Enable [versioning](https://docs.jetadmin.io/user-guide/version-control) to publish releases and restore a previous state. Releases require a paid plan.

## Common questions

### Do I need an existing database?

No. You can create tables in Jet Tables or import data from a supported file.

### Where do I enter AI prompts?

Use the custom component builder for interfaces, Ask AI for queries and API requests, and Ask AI in the workflow builder for workflow steps.

### Can I use the app with external customers?

Yes. Use the customer portal guide and configure sign-in and permissions for your users.

### What if something doesn't work?

Check [FAQ and troubleshooting](https://docs.jetadmin.io/faq-and-troubleshooting). For a generated component or query, refine the prompt with the relevant fields, expected behavior, and error details.
