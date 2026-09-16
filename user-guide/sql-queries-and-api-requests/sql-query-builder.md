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
WHERE "Opened date" >= '2019-01-01'
  AND "Opened date" < '2020-01-01'
  AND priority = 'Low';
```

{% @arcade/embed url="https://app.arcade.software/share/B1cUtKdZJcMZRr2xFKuv" flowId="B1cUtKdZJcMZRr2xFKuv" %}

Use the table and field names shown in your resource. Replace `'Low'` with the exact priority value stored in your table. The query includes every date in 2019 and excludes other priorities. Review generated SQL before running it.

{% @arcade/embed url="https://app.arcade.software/share/NvrLmzZbiySNDqwW11WS" flowId="NvrLmzZbiySNDqwW11WS" %}

### Inserting Tables and Columns

On the right-hand panel, you will see a list of all available tables and their columns. By clicking on any table or column, it is automatically inserted into your SQL editor. This eliminates the need to manually type table names or remember exact column names, reducing errors and making query construction much faster.

<figure><img src="https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2FcyvOl53QBOiGCfHvVwf5%2Fimage.png?alt=media&#x26;token=026d6bd8-a024-4858-bc09-10b81ae95952" alt="SQL Query Builder configuration"><figcaption></figcaption></figure>

### Inserting Custom Inputs

The Query Builder also allows you to add dynamic parameters using the **Insert Input** option below the editor. Inputs act as placeholders for values that can change, so you can reuse the same query multiple times with different filters. This is particularly handy when running similar queries across different date ranges or user IDs without rewriting SQL each time.

<figure><img src="https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2FpT7Zfg5pxgw1D0Mlf0XJ%2Fimage.png?alt=media&#x26;token=050e75f1-3884-474d-bd53-78ce63d39f93" alt="SQL Query Builder configuration"><figcaption></figcaption></figure>

{% hint style="info" %}
### Prettify SQL

Click **Prettify SQL** to automatically format your query, making it more readable and easier to debug.
{% endhint %}

### Transforming Query Results

After running a query, use the **Transform** feature to adjust results. Choose from dropdown options or write custom JavaScript. AI can also generate transformation code to rename fields, restructure data, or filter results.

{% @arcade/embed url="https://app.arcade.software/share/NMcY31rHAKf7igivIPLV" flowId="NMcY31rHAKf7igivIPLV" %}

### Testing, Previewing, and Saving

Click **Test Request** to run your query and check the results in the **Preview panel**. Once everything looks correct, click **Save** to reuse the query later—ideal for recurring reports or analysis.

{% hint style="info" %}
### Verify the result

Test records at the start and end of 2019, one record outside that year, and one with a different priority. Only low-priority records from 2019 should appear.
{% endhint %}

For a reusable filter, follow [Use dynamic SQL inputs](use-dynamic-sql-inputs.md).
