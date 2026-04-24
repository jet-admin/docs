---
description: >-
  Agents in JetAdmin can use different AI models depending on the task,
  performance needs, and cost considerations.
---

# AI Models

#### Available Models

<table data-header-hidden data-full-width="false"><thead><tr><th></th><th></th><th></th><th></th></tr></thead><tbody><tr><td><strong>Anthropic (Claude)</strong></td><td><strong>OpenAI</strong></td><td><strong>Google (Gemini)</strong></td><td><strong>Self-hosted</strong></td></tr><tr><td>Claude 4.6 Opus</td><td>GPT 5.x (full)</td><td>Gemini 3.1 Pro</td><td>Llama</td></tr><tr><td>Claude 4.5 Opus</td><td>GPT 4.x (full)</td><td>Gemini 2.5 Pro</td><td>Mistral</td></tr><tr><td>Claude 4.1 Opus</td><td>GPT Mini</td><td>Gemini 3.1 Flash</td><td>Qwen</td></tr><tr><td>Claude 4.5 Sonnet</td><td>GPT Nano</td><td>Gemini 2.5 Flash</td><td>DeepSeek</td></tr><tr><td>Claude 4 Sonnet</td><td>Codex</td><td></td><td></td></tr><tr><td>Claude 4.5 Haiku</td><td></td><td></td><td></td></tr></tbody></table>

{% hint style="info" %}
#### Understanding Model Trade-offs

Faster models are more cost-efficient and ideal for simple, high-volume tasks.\
More advanced models provide better reasoning, accuracy, and context handling, but consume more credits.
{% endhint %}

{% tabs fullWidth="false" %}
{% tab title="Budget Models" %}
Best for fast responses and high-volume, low-cost tasks.

| **Model**              | **Used For**                                        |
| ---------------------- | --------------------------------------------------- |
| Claude 4.5 Haiku       | Quick responses, simple automation, chat assistants |
| Gemini Flash (2.5–3.1) | Lightweight tasks, fast lookups, basic workflows    |
| OpenAI Nano            | Short prompts, formatting, simple text handling     |
| Llama (small)          | Basic self-hosted tasks with minimal complexity     |
{% endtab %}

{% tab title="Advanced Models" %}
Balanced performance for most business use cases.

| **Model**            | **Used For**                                   |
| -------------------- | ---------------------------------------------- |
| Claude 4.5 Sonnet    | General-purpose agents, multi-step tasks       |
| Gemini Pro (2.5–3.1) | Data analysis, structured workflows            |
| OpenAI Mini          | Reliable automation, moderate reasoning tasks  |
| Mistral / Qwen       | Mid-level self-hosted workloads and processing |
{% endtab %}

{% tab title="Expert Models" %}
Best for complex reasoning, critical tasks, and high accuracy.

| **Model**                             | **Used For**                                       |
| ------------------------------------- | -------------------------------------------------- |
| Claude 4.1 / 4.5 / 4.6 Opus           | Deep analysis, complex decision-making             |
| OpenAI 5.x / 4.x (full models, Codex) | Advanced logic, coding, multi-step reasoning       |
| Gemini Pro (latest versions)          | Large context tasks, high-accuracy outputs         |
| DeepSeek / large Llama                | Advanced self-hosted reasoning and heavy workloads |
{% endtab %}
{% endtabs %}

{% hint style="info" %}
#### Choosing Models & Managing Costs

Start with budget or advanced models for most use cases, they are faster and more cost-efficient.\
Move to expert models only when tasks require deeper reasoning, higher accuracy, or complex logic.

To reduce credit usage:

* Use simpler models for repetitive or low-complexity tasks
* Keep instructions clear to avoid unnecessary retries
* Limit unnecessary tool calls or repeated executions

A good approach is to start simple, test performance, and only scale up when needed.
{% endhint %}

{% hint style="success" %}
#### Managing Credits

You can track your credit usage and manage your balance from your account:

* **Usage page** (Profile → Usage) to monitor consumption
* **Billing page** to add or purchase more credits
{% endhint %}

