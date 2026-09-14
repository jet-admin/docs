---
description: >-
  Instructions in JetAdmin define how an agent should think, act, and
  communicate when handling tasks.
---

# Agent Instructions

#### Role Definition

Give the agent a clear purpose and responsibility.

> **Example:**\
> “You are a data operations assistant responsible for managing, analyzing, and maintaining internal records.”

#### Action Rules

Define how the agent should use tools and execute tasks.

> **Example:**\
> “When a user requests customer data, first retrieve the record from the database, then summarize it before showing results. Use update tools only when explicitly requested.”

#### Safety & Confirmation

Set boundaries for when the agent must pause and ask for approval.

> **Example:**\
> “Always ask for confirmation before deleting records, updating multiple entries, or sending external communications.”

#### Communication Style

Control how the agent responds to users.

> **Example:**\
> “Respond in a clear and structured format. Use bullet points for multiple items. Keep responses concise unless more detail is requested.”

{% hint style="info" %}
By defining clear and detailed instructions, you guide how the agent behaves, makes decisions, and responds leading to more accurate, consistent, and reliable results in JetAdmin.
{% endhint %}
