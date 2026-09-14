---
description: >-
  Learn how to use Jetadmin Agents to automate tasks using natural language and
  LLMs, no coding or complex logic required.
icon: message-bot
---

# Agents

### What Are Agents?

Agents in JetAdmin are AI components that can understand a task, decide what actions to take, and execute them using available tools. They don’t rely on fixed steps instead, they determine the best way to complete a task based on your instructions and context.

### Key Characteristics

* **Decision-based**: choose actions instead of following fixed logic
* **Action-oriented**: use tools, workflows, and data to get things done
* **Interactive**: can be triggered through chat or other inputs
* **Contextual:** use instructions and past input to guide behavior

### Creating Your First Agent

{% stepper %}
{% step %}
#### Add an Agent

Add an agent to your app in JetAdmin using one of the following:

* Add it as a **component** from the components panel
* Create it inside a **workflow** using a trigger or step
* Use the **Agents section** from the left sidebar

{% content-ref url="add-an-agent.md" %}
[add-an-agent.md](add-an-agent.md)
{% endcontent-ref %}
{% endstep %}

{% step %}
#### Add Tools

Connect the tools your agent will use to perform actions.

This can include:

* **Data sources** (e.g. Airtable, Supabase, internal tables)
* **Integrations** (e.g. APIs, external services)
{% endstep %}

{% step %}
#### Write Instructions

Define how the agent should behave and what it should do. Keep instructions clear and specific to get better results.

Example (Data Manager Agent):

```
You're a data management assistant responsible for working with application data.

Your responsibilities:
1. Retrieve and display data based on user requests
2. Create new records when instructed
3. Update existing records with clear confirmation
4. Delete records only after explicit user approval
5. Analyze data and provide insights when requested

Guidelines:
- Always confirm before making changes that affect data
- Ensure accuracy when reading or modifying records
- Clearly explain any updates or actions performed
- If the request is unclear or incomplete, ask for clarification
```
{% endstep %}

{% step %}
#### Test Thoroughly

Run the agent with different inputs to make sure it:

* Understands the task
* Uses the correct tools
* Produces reliable results
{% endstep %}
{% endstepper %}

### How Agents Work

Agents in JetAdmin combine instructions, tools, and built-in decision logic to figure out the best way to complete a task, one step at a time.

{% @arcade/embed flowId="shdqfKBJ6wLtfV5WnaLm" url="https://app.arcade.software/share/shdqfKBJ6wLtfV5WnaLm" %}

{% hint style="info" %}
### Agents vs Workflows

* **Agents:** dynamic, decide the next step
* **Workflows:** predefined, execute fixed steps

Agents can use workflows when structured execution is needed.
{% endhint %}
