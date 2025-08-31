---
description: >-
  The SQL Query Builder lets you create, edit, and run queries easily. You can
  write SQL manually, insert tables and columns, or let AI generate queries and
  transformations for you.
---

# SQL Query Builder

### Writing and Generating Queries

You can type SQL directly in the editor or click **Ask AI** to describe what you need in plain language. AI will generate the SQL for you—for example, _“show tickets created in 2019 with low priority.”_

```sql
SELECT *
FROM Tickets
WHERE "Opened date" BETWEEN '2018-01-01' AND '2024-12-31';
```

{% @arcade/embed flowId="B1cUtKdZJcMZRr2xFKuv" url="https://app.arcade.software/share/B1cUtKdZJcMZRr2xFKuv" %}

Or consider using AI to refine or write your SQL query for enhanced accuracy and efficiency.

{% @arcade/embed flowId="NvrLmzZbiySNDqwW11WS" url="https://app.arcade.software/share/NvrLmzZbiySNDqwW11WS" %}

### Inserting Tables and Columns

On the right-hand panel, you will see a list of all available tables and their columns. By clicking on any table or column, it is automatically inserted into your SQL editor. This eliminates the need to manually type table names or remember exact column names, reducing errors and making query construction much faster.

<figure><img src="../../.gitbook/assets/image (981).png" alt=""><figcaption></figcaption></figure>

### Inserting Custom Inputs

The Query Builder also allows you to add dynamic parameters using the **Insert Input** option below the editor. Inputs act as placeholders for values that can change, so you can reuse the same query multiple times with different filters. This is particularly handy when running similar queries across different date ranges or user IDs without rewriting SQL each time.

<figure><img src="../../.gitbook/assets/image (982).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
### Prettify SQL

Click **Prettify SQL** to automatically format your query, making it more readable and easier to debug.
{% endhint %}

### Transforming Query Results

After running a query, use the **Transform** feature to adjust results. Choose from dropdown options or write custom JavaScript. AI can also generate transformation code to rename fields, restructure data, or filter results.

{% @arcade/embed flowId="NMcY31rHAKf7igivIPLV" url="https://app.arcade.software/share/NMcY31rHAKf7igivIPLV" %}

### Testing, Previewing, and Saving

Click **Test Request** to run your query and check the results in the **Preview panel**. Once everything looks correct, click **Save** to reuse the query later—ideal for recurring reports or analysis.

{% hint style="info" %}
### Best Practices

To get the most out of the SQL Query Builder, it’s a good idea to prettify queries regularly for readability, and make frequent use of AI assistance for complex SQL generation. Inputs should be used whenever possible to create dynamic, reusable queries. Transformations are a powerful way to adjust your results without altering the base SQL, and testing queries before saving ensures accuracy. Finally, previewing results after execution helps confirm that your query meets the intended goals.
{% endhint %}
