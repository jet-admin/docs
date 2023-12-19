---
description: In this section, you will learn how to create custom fields using Formulas
---

# Create Custom fields using Formulas

In this use case, we will create a custom column in the Customer table and calculate a score depending on some logical condition.

1\. Simply create a new Custom field in the columns settings of the table component.&#x20;

2\. Now we should configure the Value for that Column using Formulas. We will use `IF` the function to calculate the Score value, depending on the Activities number for each customer:

`=IF(item.activities < 280, '50 points', IF(item.activities < 400, '70 points', '100 points'))`

![](../../../.gitbook/assets/testgif53.gif)
