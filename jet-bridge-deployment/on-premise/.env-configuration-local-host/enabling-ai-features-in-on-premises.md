---
description: >-
  Enable and configure AI assistants in on-premises environments by adding
  required environment variables.
---

# Enabling AI Features in On-Premises

AI assistant functionality is not enabled by default in on-premises deployments. To use AI-powered features, you must configure environment variables in your env file.

### **Requirements**

* Ability to modify environment variables
* Ability to restart or redeploy the application
* Access to external AI provider APIs

{% stepper %}
{% step %}
### Add AI Configuration

Add the following variables to your environment configuration:

```dotenv
#------------------------------------------------------------------------------
# AI parameters (must be configured)
#------------------------------------------------------------------------------
ASSISTANTS_ENABLED=1
OPENAI_API_KEY=your_openai_api_key
OPENAI_MAX_TOKENS=1024
ANTHROPIC_API_KEY=
```

> Enables AI assistant functionality.
>
> * `0` — Disabled (default)
> * `1` — Enabled
>
> You must set this to `1` to activate any AI features.
{% endstep %}

{% step %}
### Configure Parameters

AI features rely on external AI providers. The provider you configure determines which features are available and how they behave.

{% hint style="info" %}
#### Feature-Based Provider Usage

* Ask AI feature: Requires Anthropic
* Agents: Supports Anthropic and OpenAI

If you are not using one of these providers, you can leave its configuration empty.
{% endhint %}

#### **Anthropic (Required for Ask AI)**

To use the Ask AI feature, you must configure Anthropic:

```
ANTHROPIC_API_KEY=your_anthropic_api_key
```

#### **OpenAI**&#x20;

OpenAI can be used with **Agents**.

```
OPENAI_API_KEY=your_openai_api_key
OPENAI_MAX_TOKENS=1024
```

#### **Using Agents with Multiple Providers**

If both providers are configured:

```
ANTHROPIC_API_KEY=your_anthropic_api_key
OPENAI_API_KEY=your_openai_api_key
```

{% hint style="success" %}
💡 **Flexible Model Selection**\
When both Anthropic and OpenAI are configured, users can choose which provider (model) an Agent uses directly within JetAdmin.
{% endhint %}
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
#### Notes

* At least one AI provider API key must be configured when `ASSISTANTS_ENABLED=1`
* Ensure outbound network access to AI providers (e.g., OpenAI, Anthropic) is allowed
{% endhint %}
