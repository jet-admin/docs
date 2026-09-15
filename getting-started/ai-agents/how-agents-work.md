---
description: >-
  Understand how Jetadmin Agents operate behind the scenes, breaking down the
  step-by-step reasoning cycle that drives their decision-making and actions.
---

# How Agents Work

**The Agent Process**

When an agent is triggered, it follows a structured reasoning cycle to complete its task:

**1. Task Input**\
The agent receives clear instructions in plain language—for example, _“Find all overdue invoices and email the client.”_

**2. Decision Making with LLM**\
The large language model determines the next step, which could be:

* Responding directly to the task,
* Asking for more information, or
* Activating a connected tool such as a data source, workflow, email, or even another agent.

**3. Tool Execution**\
The chosen tool performs its action, and the results are sent back to the LLM for further processing.

**4. Agentic Loop**\
This cycle of decisions and tool executions repeats until:

* The agent reaches its maximum allowed steps, or
* The LLM concludes that the task is complete.

Each complete cycle—from input to reasoning to output—is called a **run**.

{% hint style="info" %}
⚡ **Key Point:** The LLM’s role is limited to either calling tools repeatedly or providing the final response.
{% endhint %}
