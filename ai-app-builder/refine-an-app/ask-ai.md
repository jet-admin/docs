---
description: >-
  Ask AI enables you to work with APIs, SQL, data transformations, and much
  more, all through simple natural language prompts.
icon: brain-circuit
---

# Ask AI for queries and transformations

The Ask AI feature converts plain text instructions into working API requests, SQL queries, transformation scripts, and a variety of other outputs. Review and test the generated output against your source schema and expected results before using it in the app.

### Ask AI for API

Ask AI simplifies working with APIs. You can type a request in plain English, provide a curl command, or link to Swagger documentation, and it can draft an API call for you to inspect and test.

**What it can do:**

* Generate API requests from text, curl, or docs
* Suggest fixes for failed requests
* Transform responses into structured outputs
* Handle pagination and sorting automatically

**Examples:**

* _“Get Deals with status = 'Won'”_ → Collection API call

{% @arcade/embed url="https://app.arcade.software/share/p0HlAH9LXWUdga7FW0xL" flowId="p0HlAH9LXWUdga7FW0xL" %}

{% hint style="warning" %}
Always double-check sensitive API actions (like refunds or deletions) before running them. Ask AI generates requests automatically, but execution is final.
{% endhint %}

### Ask AI for SQL

Instead of writing queries manually, you can describe what you need and Ask AI creates the SQL for you. If the result fails, provide the error and expected output in a focused follow-up.

**What it can do:**

* Translate text prompts into SQL queries
* Detect and fix SQL errors
* Transform results for dashboards or reports

**Example:**

* _“Get all transactions/orders where the amount > 100”_ → SQL query

{% @arcade/embed url="https://app.arcade.software/share/2GwPGjj0QLrr8MgYBt5s" flowId="2GwPGjj0QLrr8MgYBt5s" %}

{% hint style="info" %}
If the generated query looks too broad, try refining your prompt with additional filters (e.g., date ranges or specific columns)
{% endhint %}

### Ask AI for Transformations

Ask AI also supports transformations, making it easier to work with complex or nested data. You can quickly create or debug scripts without needing to code them from scratch.

**What it can do:**

* Flatten nested JSON or API responses
* Generate custom JavaScript transformations
* Fix broken transformation logic

**Example:**

* _“_&#x46;ilter the API response to keep only these key fields: Service, Entity/Resource, Action Type, Endpoint URL, and Filters/Parameters._”_ → JavaScript transformation

{% @arcade/embed url="https://app.arcade.software/share/AAu2Wu3r2tHwVueJh6fm" flowId="AAu2Wu3r2tHwVueJh6fm" %}

{% hint style="info" %}
To get the most out of Ask AI, keep these tips in mind:

* **Be specific in your prompts.** The more details you give (fields, filters, conditions), the more accurate the output will be.
* **Always review before running.** Check generated API calls, SQL queries, or scripts especially if they modify or delete data.
* **Test safely first.** Run queries or actions on test data before applying them to production.
* **Iterate step by step.** If the first result isn’t perfect, refine your prompt instead of starting over.
* **Use hints and context.** Linking docs, curl commands, or schemas can help Ask AI generate better results.
{% endhint %}

## Check the result

Test a read-only request first. Compare returned fields, filtering, and record counts with a known test case. For a write request, inspect the method, destination, inputs, and permissions before execution.

Continue with [App Console and logs](../preview-and-troubleshoot/inspect-app-console-and-logs.md) for Preview diagnostics.
