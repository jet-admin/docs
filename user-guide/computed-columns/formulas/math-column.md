---
description: Perform instant calculations using the data in your project
---

# Math Column

Let's suppose you need to calculate the total cost by multiplying the Price and Quantity fields:

1. Click on the `Add Column` icon -> `Add Computed Column`
2. Rename the Field
3. Click on the `Set up with Formula` icon
4. Now we should configure the Value for that Column. We will use the \* operation to calculate the Total cost value: `=item.Cost * item.Amount`
5. Now let's concatenate the Total cost with the currency $ using the CONCAT() function: `=CONCAT("$", item.Price * item.Quantity)`

{% @arcade/embed flowId="Msh0uH5NGTgs7yvedjrG" url="https://app.arcade.software/share/Msh0uH5NGTgs7yvedjrG" %}
