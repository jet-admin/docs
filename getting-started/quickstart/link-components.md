# Link Components

To create custom **user flows** in your app, you need to be able to pass values between components. For this, Jet Admin has the `Formulas` modal window, where you can map the components:

![](<../../.gitbook/assets/Screenshot (31).png>)

In our example, we need the `Stage` and the `Amount` values to be fetched from the selected customer in the `Customers` table:

![](../../.gitbook/assets/Quickstart-components7.gif)

Now, let's set up an **action** that will `update` our customer record with the input values:

{% content-ref url="configure-an-action.md" %}
[configure-an-action.md](configure-an-action.md)
{% endcontent-ref %}
