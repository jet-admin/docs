---
description: >-
  Jet Admin’s AI can automatically generate the parameters and actions your
  custom component needs — based entirely on your prompt.
---

# Auto-Generate Parameters and Actions

<figure><img src="../.gitbook/assets/Frame 8473-min.jpg" alt=""><figcaption></figcaption></figure>

### How It Works

1.  **Write a Clear Prompt**\
    Describe what your component should do, including any fields or interactions.\
    Example:

    > "A user profile card showing name, email, and a button to send a message."
2. **Let the AI Auto-Generate**\
   After processing your prompt, Jet Admin automatically:
   * **Creates parameters** (e.g., `name`, `email`, `profileImage`)
   * **Adds actions** (e.g., `sendMessage` function on button click)
3. **Review and Customize**\
   Once generated:
   * Review the parameters and actions.
   * Adjust or rename them if needed.

{% @arcade/embed flowId="Qix2MXQkru95sk9RSGEs" url="https://app.arcade.software/share/Qix2MXQkru95sk9RSGEs" %}

{% hint style="info" %}
### 📋 Best Practices

**Mention Actions Clearly in Your Prompt**:\
If you want something clickable or interactive, make sure to say it.

**Use Descriptive Names**:\
Good field names (like `userName` instead of just `text`) help with clean, understandable code.

**Check and Test**:\
Always preview your generated actions to ensure they behave as expected.
{% endhint %}
