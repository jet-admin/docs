---
description: >-
  Learn how to trigger and run Agents in Jetadmin manually via the UI, through
  workflows, or by chaining agents together for seamless automation.
---

# Running Agents

Agents don’t run on their own—they need to be **triggered manually or programmatically** using one of the following methods:

* **Agent Chat Component:** Add this to your app’s UI to let users interact with the agent directly.

{% @arcade/embed flowId="npghiU9hNeEStFMmKARQ" url="https://app.arcade.software/share/npghiU9hNeEStFMmKARQ" %}

* **Ask Agent Action:** Use this Action within workflows or automations to run the agent at the right moment.

<figure><img src="../.gitbook/assets/image (983).png" alt=""><figcaption></figcaption></figure>

* **Another Agent:** You can chain agents together, allowing one agent to call another as part of its logic.

<figure><img src="../.gitbook/assets/image (984).png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
**Note:** To run an agent automatically—such as on a schedule or after receiving a webhook—you'll need to create an Automation that includes the **Invoke Agent** block.
{% endhint %}

{% content-ref url="../user-guide/workflow/page-1.md" %}
[page-1.md](../user-guide/workflow/page-1.md)
{% endcontent-ref %}

{% content-ref url="../user-guide/workflow/" %}
[workflow](../user-guide/workflow/)
{% endcontent-ref %}
