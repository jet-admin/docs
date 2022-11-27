---
description: Parse JSON
---

# Parse JSON Fields

Suppose you have a field that stores data in JSON format. You can display the desired data in a separate column. The JSON structure is shown in the example:&#x20;

```javascript
{
  "fields": {
    "pricing": {
      "integerValue": "109"
    },
    "quantity": {
      "integerValue": "98"
    }
  }
}
```

1\. Simply create a new Custom field in the columns settings of the table component:

![](../../../.gitbook/assets/testgif80.gif)

2\. Now let's display the Pricing value in a separate column. For the JSON structure shown in the example above, you need to use the following value:

`=item.order.fields.pricing.integerValue`

![](../../../.gitbook/assets/testgif81.gif)

Now your data is displayed in a clear and readable way in a separate column.

{% hint style="info" %}
Note that the value may differ depending on the JSON field structure.
{% endhint %}
