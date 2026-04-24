---
description: >-
  Agents in JetAdmin can be used inside workflows to add decision-making and
  flexibility to structured automations.
---

# Workflows with Agents

### How Agents Fit into Workflows

Workflows handle defined steps, while agents evaluate context and determine the next action during execution. This allows you to build multi-step processes that can adapt without relying on complex conditional logic.

#### Example: Processing Orders from Input

In this example, a user submits order details through the app, and a workflow uses an agent to process and store the data.

{% stepper %}
{% step %}
#### Add Input Components

Add the following to your app in JetAdmin:

* A **multi-line text input** (for order details)
* A **button** (e.g. “Process Order”)

<figure><img src="../.gitbook/assets/image (991).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Configure the Trigger

Set the button action to:

* Trigger a **workflow**
* Pass the text input as a parameter

{% content-ref url="../user-guide/workflow/page-1.md" %}
[page-1.md](../user-guide/workflow/page-1.md)
{% endcontent-ref %}
{% endstep %}

{% step %}
#### Build Workflow Steps

In the workflow canvas:

1. **Agent: Process Input**
   * Read the submitted text
   * Extract structured order data (e.g. name, items, quantity)
   * Clean and format the data
2. **Create Record**
   * Save the structured data into the Orders table
3. **Send Email**
   * Generate a confirmation message
   * Send it to the customer or internal team

<figure><img src="../.gitbook/assets/image (990).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Test the Workflow

Enter sample order data and click the button to verify:

* The agent correctly parses and structures the input
* The record is created in the database
* The email is generated and sent successfully
{% endstep %}
{% endstepper %}

### Why Use Agents in Workflows

Workflows provide structured execution, while agents introduce flexible decision-making.

Together, they enable automations that are both reliable and adaptable without requiring complex logic or extensive conditions.

{% hint style="success" %}
#### Agent Chaining

In more advanced setups, multiple agents can work together.

You can create specialized agents for different tasks and use them as tools within a main agent. The main agent can then delegate specific responsibilities to sub-agents when needed.

Clear and focused instructions for each agent are essential to ensure reliable coordination.
{% endhint %}
