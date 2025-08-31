---
description: Creating workflows using the Ask AI feature
---

# Workflows with AI

With AI-powered workflow creation, you can quickly generate workflows by simply describing them in plain English. The AI automatically builds the required steps, which you can then customize to match your exact needs.

#### Creating a Workflow with AI

To add a workflow, start by choosing any trigger action such as a button click, data change, page load, or any other supported trigger. \
Once the workflow builder is open, Click on the **Ask AI**. In the AI chat, type your request in natural language and wait for the AI to generate the workflow based on your input.

{% content-ref url="page-1.md" %}
[page-1.md](page-1.md)
{% endcontent-ref %}

{% @arcade/embed flowId="Sd6L8bPYmjApw4sEQ7on" url="https://app.arcade.software/share/Sd6L8bPYmjApw4sEQ7on" %}

{% hint style="info" %}
#### 💡 Reviewing and Customizing the Workflow

> After AI generates the workflow, always review the steps it has created. You may need to apply small adjustments to better fit your application needs. Typical customizations include configuring your data sources, setting up conditions, or adding additional actions to refine the workflow.
{% endhint %}

#### Example Workflow

For example, you can ask AI to create a workflow that checks the **Customer** table in the **Agent** data source. If there is any customer where the `customer-type` field is equal to _new_, the workflow should automatically send a demo call email to the customer’s email address.

You can provide an email template such as:

> **Subject:** Schedule Your Demo Call\
> **Body:** Hello \{{customer-name\}}, thank you for signing up! Please use the link below to schedule your demo call with us.

AI will generate the workflow with these steps:

* Query the Customer table to check for new customers.
* For each matching record, trigger an email action.
* Insert customer-specific values (such as name and email) into the template.

From there, you can review and customize the workflow as needed — for instance, by adjusting the query conditions or refining the email template.

{% @arcade/embed flowId="kIdVDgdbOWiisMcS83oy" url="https://app.arcade.software/share/kIdVDgdbOWiisMcS83oy" %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-08-31 165254.png" alt=""><figcaption></figcaption></figure>
