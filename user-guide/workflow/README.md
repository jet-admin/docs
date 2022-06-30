# ⚙️ Automations

**Automations** allow you to create a sequence (or workflow) of events that is executed based on a  specific trigger. Workflows consist of triggers and steps.

Here's an **example** of a workflow that is triggered when a button is clicked and then it either creates a record in Airtable or shows a notification based on whether the "Yes/No" condition is met.

![](../../.gitbook/assets/zsrhxd.png)

## Overview

The workflow builder consists of several **key parts**:

**(1) Triggers** determine when (on what condition) the workflow will run. For example, this might be a button click or a row click in a table.&#x20;

**(2) Steps** consist of **actions**, which run in a sequential manner when a workflow is triggered, and **rules**, which allow you to branch the sequence based on certain conditions. An example of an action would be "Updating a record in Airtable" and an example of a rule could be "If condition" that will divide a workflow into two branches.&#x20;

**(3)** You can add **new steps** before or after any step, just click the "+" icon

**(4)** **Workflow result** closes the sequence and can be used to configure the workflow outputs

**(5)** The **configuration tab** that opens up when you select a trigger or a step

![](../../.gitbook/assets/xtjcfh.png)

## When to use it

For the most part, you'll need a single action, such as `changing a status` or `making a refund`. However, in specific cases, you'll need a whole sequence of actions to be executed, often with conditional logic.

To give an overview of what can be achieved with automations, here's the list of common tasks for them:

Interface

## Triggers

To start building automation, **select the trigger** which will initiate it. Triggers can be broadly divided into three categories:&#x20;

* Buttons
* List actions
* Success/Error actions

#### Buttons

The most common one is `button`. To create an automation, click on the "Click action" **(1)** and then choose "Run Workflow" **(2)**.

![](../../.gitbook/assets/srgzx.png)

#### List Actions

You can also create automation for any of the **list actions**. The lists include `Table`, `Map`, `Kanban`, `Gallery`, `Timeline`, and `Calendar`.

![](../../.gitbook/assets/szbdx.png)

#### Success/Error actions

Another type of an action that can trigger workflows is `Success/Error`:

![](<../../.gitbook/assets/rshzdxctfy (1).png>)

In all the cases, you'll need to choose the "**Run workflow**" type of action:

![](<../../.gitbook/assets/image (878).png>)

## Actions



## Rules

Inputs, Outputs, and Parameters





As the company is growing and the roles are diversifying, the need for some sort of a task management system for your internally-facing applications is increasing. So we came up with the **Approval Workflow** feature.

{% content-ref url="task-approval.md" %}
[task-approval.md](task-approval.md)
{% endcontent-ref %}

In JetAdmin you can create **Actions Workflow** that allow you to perform multiple actions immediately after performing the base action.

{% content-ref url="actions-workflow.md" %}
[actions-workflow.md](actions-workflow.md)
{% endcontent-ref %}

Create a **sequence of actions** in Zapier or Integromat by triggering through JetAdmin actions.

{% content-ref url="action-sequences.md" %}
[action-sequences.md](action-sequences.md)
{% endcontent-ref %}
