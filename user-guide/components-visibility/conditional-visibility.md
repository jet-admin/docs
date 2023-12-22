---
description: In this section you will learn about Conditional Visibility
---

# Conditional Visibility

Conditional Visibility allows you to **dynamically show/hide** a UI component based on a rule.&#x20;

To enable it, you'll have to write a formula in the "Conditional visibility" box.

{% hint style="warning" %}
**You don't have to** write an "IF" expression to make it work. Simply `EQ(A, B)`will make the field visible when the variables meet the condition (A=B) and invisible when the opposite is true (under the hood it will return logical "1" and "0" correspondingly)
{% endhint %}

If the conditional visibility was enabled for a specific UI component AND the condition **is not** met, you'll see **the "eye" sign** in front of the component:

![](../../.gitbook/assets/gncvyu.png)

Here's an example of how conditional visibility works with static values:

![](../../.gitbook/assets/fxjgyn.gif)

**Static values** are more suited for demonstrating how conditional visibility works when the real use-cases most of the time involve **dynamic values**.

To use a **dynamic value**, delete one of the values in the formula (doesn't matter which one):&#x20;

![](../../.gitbook/assets/xdntcfhvy.png)

And replace it with the reference to the dynamic value. In our example, we've added to a canvas a new UI component: `Dynamic value` input **(1)** that may receive any value. After we've added it, it automatically appears in the modal window where we can reference it **(2)**.

{% hint style="info" %}
Learn more about **binding and referencing** dynamic values in the [Values section](../parameters/)
{% endhint %}

![](<../../.gitbook/assets/zrhxdct (2).png>)

After mapping the variable from the "Conditional visibility" formula onto the "Dynamic value" input component, the left component will be visible/invisible **based on the value** in the right input component:

![](../../.gitbook/assets/dnxtcfy.gif)

Not only can you fetch dynamic values from the "Input" UI components, but also "**User properties**" such as `email`, or values from specific fields from **selected rows** in the "Table" UI component.
