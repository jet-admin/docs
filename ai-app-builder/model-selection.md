---
description: >-
  Choose an AI model, switch between quick options, and compare the models
  available in Jet Admin.
icon: brain-circuit
---

# Model selection

Choose an AI model for your task, or let Jet Admin choose one automatically.

## Overview

The model selector includes quick choices and individual models from Anthropic, OpenAI, and Google. Start with **Automatic** if you do not have a model preference.

| Option      | Model                     | When to choose it                                                                       |
| ----------- | ------------------------- | --------------------------------------------------------------------------------------- |
| Automatic   | Selected for each request | Let Jet Admin choose the model for your request.                                        |
| Recommended | Claude 4.6 Sonnet         | A starting point for everyday work, such as adding features and refining an app.        |
| Smartest    | Claude 4.6 Opus           | Try this for complex logic, multi-step changes, or a problem that needs more reasoning. |
| Fastest     | Gemini 3 Flash            | Use this when quick responses matter, such as small edits and short iterations.         |

These shortcuts reflect the options in the model selector. You can also choose a specific model from the provider sections.

## How to switch models

1. Open the model selector in the AI conversation.
2. Choose **Automatic**, **Recommended**, **Smartest**, or **Fastest**. To select a specific model, browse the provider sections or use **Search**.
3. Select the model, then send your next request.

If you are unsure which model to choose, start with **Automatic**. For a focused change, describe the exact result you want. If the result needs improvement, clarify the request or try **Smartest**, then review the generated changes.

## Available models

The following list reflects the model selector as of September 16, 2026. Check the selector for the options currently available to you.

### Anthropic

| Model             | Context window shown |
| ----------------- | -------------------- |
| Claude 4.6 Sonnet | 1M                   |
| Claude 4.6 Opus   | 1M                   |
| Claude 4.5 Sonnet | 1M                   |
| Claude 4.5 Opus   | 200K                 |
| Claude 4.5 Haiku  | 200K                 |
| Claude 4.1 Opus   | 200K                 |
| Claude 4 Sonnet   | 1M                   |

### OpenAI

| Model         | Context window shown |
| ------------- | -------------------- |
| GPT-5.4       | 1M                   |
| GPT-5.4 Mini  | 400K                 |
| GPT-5.4 Nano  | 400K                 |
| GPT-5.3 Codex | 400K                 |
| GPT-5.2       | 400K                 |
| GPT-5.2 Codex | 400K                 |
| GPT-5.1       | 400K                 |
| GPT-5         | 400K                 |
| GPT-5 Mini    | 400K                 |
| GPT-5 Nano    | 400K                 |
| GPT-4.1       | 1M                   |
| GPT-4.1 Mini  | 1M                   |

### Google

| Model            | Context window shown |
| ---------------- | -------------------- |
| Gemini 3.1 Pro   | 1M                   |
| Gemini 3 Pro     | 1M                   |
| Gemini 3 Flash   | 1M                   |
| Gemini 2.5 Pro   | 1M                   |
| Gemini 2.5 Flash | 1M                   |

### Self-hosted models

Self-hosted models are available only on the **Enterprise plan**.

The **Self-hosted models** section includes **Llama**, **Mistral**, **Qwen**, and **DeepSeek**. Open a family to see its model options.

## Understanding context windows

The number beside a model indicates its context window, measured in tokens: **200K** means 200,000 tokens, **400K** means 400,000, and **1M** means one million.

A context window is the amount of information a model can work with in a request, including instructions and conversation content. A larger window can accommodate more context; it does not guarantee a better answer or represent a file-upload limit. Keep requests focused and provide the information needed for the task.

## Credits and usage

Model choice and task complexity affect AI usage. The selector's context-window numbers are not credit prices. For your remaining allowance, check your account's usage and billing information.

See How credits work for AI building credits, or AI Models for guidance on choosing models for agents.
