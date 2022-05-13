# Conditional Disable

Conditional Disable allows you to show the value of the field (input) but make it **dynamically uneditable** based on a rule.&#x20;

To enable it, you'll have to write a formula in the "Conditional disable" box.

{% hint style="warning" %}
**You don't have to** write an "IF" expression to make it work. Simply A=B or A>B will make the field disabled (uneditable) for when the variables meet the condition and enabled (editable) when the opposite is true (under the hood it will return logical "1" and "0" correspondingly)
{% endhint %}

