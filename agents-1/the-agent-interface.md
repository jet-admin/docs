---
description: >-
  Explore the key sections of the Jetadmin Agent configuration interface, where
  you define your agent’s purpose, inputs, behavior, and access to tools.
---

# The Agent Interface

When configuring an agent, you’ll find these  key sections:

1. **Instruction**
   * Define the main goal or purpose of the agent.
   * Example: _“Act as a customer support assistant that answers product-related questions.”_
2. **Agent Inputs**
   * Provide custom input fields that can be referenced inside instructions.
   * Useful for passing dynamic data into the agent’s reasoning.
3. **Additional Settings**
   * **Steps Maximum**: limit the number of reasoning loops (up to 30).
   * **Temperature**: adjust randomness (lower = more predictable, higher = more creative).
4. **Tools Available to Agent**
   * Choose which tools the agent can use (data sources, actions, other agents, etc.).
   * Add tool-specific instructions to guide behavior.
   * Control permissions (CRUD levels) for each tool.

{% @arcade/embed flowId="RQdtlMFTx4VSejQcbVZU" url="https://app.arcade.software/share/RQdtlMFTx4VSejQcbVZU" %}

{% hint style="info" %}
**Key Considerations for Agent Setup**\
Effective agents start with clear and detailed configuration. Providing precise instructions, well-defined inputs, and carefully selected settings and tools ensures your agent performs accurately and reliably.
{% endhint %}
