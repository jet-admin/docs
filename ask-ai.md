---
description: >-
  Ask AI enables you to work with APIs, SQL, data transformations, and much
  more, all through simple natural language prompts.
icon: brain-circuit
---

# Ask AI

The Ask AI feature converts plain text instructions into working API requests, SQL queries, transformation scripts, and a variety of other outputs. It saves time, reduces errors, and delivers clean, usable results, all without the need to remember complex syntax.

### Ask AI for API&#x20;

Ask AI simplifies working with APIs. You can type a request in plain English, provide a curl command, or link to Swagger documentation, and it will generate the correct API call.

**What it can do:**

* Generate API requests from text, curl, or docs
* Suggest fixes for failed requests
* Transform responses into structured outputs
* Handle pagination and sorting automatically

**Examples:**

* _“Get Deals with status = 'Won'”_ → Collection API call

{% @arcade/embed flowId="p0HlAH9LXWUdga7FW0xL" url="https://app.arcade.software/share/p0HlAH9LXWUdga7FW0xL" %}

{% hint style="warning" %}
Always double-check sensitive API actions (like refunds or deletions) before running them. Ask AI generates requests automatically, but execution is final.
{% endhint %}

### Ask AI for SQL

Instead of writing queries manually, you can describe what you need and Ask AI creates the SQL for you. If something doesn’t work, it fixes the query and improves readability of results.

**What it can do:**

* Translate text prompts into SQL queries
* Detect and fix SQL errors&#x20;
* Transform results for dashboards or reports

**Example:**

* _“Get all transactions/orders where the amount > 100”_ → SQL query"

{% @arcade/embed flowId="2GwPGjj0QLrr8MgYBt5s" url="https://app.arcade.software/share/2GwPGjj0QLrr8MgYBt5s" %}

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

{% @arcade/embed flowId="AAu2Wu3r2tHwVueJh6fm" url="https://app.arcade.software/share/AAu2Wu3r2tHwVueJh6fm" %}

{% hint style="info" %}
To get the most out of Ask AI, keep these tips in mind:

* **Be specific in your prompts.** The more details you give (fields, filters, conditions), the more accurate the output will be.
* **Always review before running.** Check generated API calls, SQL queries, or scripts especially if they modify or delete data.
* **Test safely first.** Run queries or actions on test data before applying them to production.
* **Iterate step by step.** If the first result isn’t perfect, refine your prompt instead of starting over.
* **Use hints and context.** Linking docs, curl commands, or schemas can help Ask AI generate better results.
{% endhint %}

{% hint style="info" %}
#### Explore More Use Cases

The examples and tips above highlight some common ways to get started with Ask AI, but the feature’s potential goes far beyond these scenarios. Whether you want to generate custom scripts, automate complex data transformations, optimize queries, or integrate with diverse APIs, Ask AI can assist in a wide variety of tasks. Feel free to experiment and discover new ways Ask AI can simplify your workflows and solve unique challenges.
{% endhint %}

{% content-ref url="user-guide/data/sql-query-builder.md" %}
[sql-query-builder.md](user-guide/data/sql-query-builder.md)
{% endcontent-ref %}

{% content-ref url="user-guide/data/api-builder/" %}
[api-builder](user-guide/data/api-builder/)
{% endcontent-ref %}

{% content-ref url="user-guide/workflow/workflows-with-ai.md" %}
[workflows-with-ai.md](user-guide/workflow/workflows-with-ai.md)
{% endcontent-ref %}
