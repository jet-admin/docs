---
description: Hide or show things based on different conditions
---

# ℹ Conditionals

Jet Admin allows you to use **conditional logic** in your app and apply it to UI components and dynamic values. There are several ways to implement it depending on the use case:

### Formulas

You can use logical expressions, such as `If`, `Else`, `Or` to transform **dynamic values**. These logical expressions live in Jet in the form of **Formulas**, which can be found in the Dynamic data modal pop-up:

![](../../.gitbook/assets/btftnf.png)

### Conditional visibility&#x20;

Component visibility allows you to **show or hide UI components** based on a rule. This might be useful, for example, when building a complex form where you want or don't want to show more fields to gather additional information based on a certain input.

Or when you want to show or hide some sections of your app depending on the user who's logged in or their role.

Conditional visibility **can be accessed** within any UI component. To access, follow the steps:

1. Click on the **Component**
2. Go to the **Display Tab**

{% @arcade/embed flowId="GTcwwla472d83KVovqMs" url="https://app.arcade.software/share/GTcwwla472d83KVovqMs" %}

Dive deeper into conditional visibility **setup** and **use cases** here:

{% content-ref url="conditional-visibility.md" %}
[conditional-visibility.md](conditional-visibility.md)
{% endcontent-ref %}

### Conditional disable

But what if you want to show the value of a UI component still, but make it **uneditable based on a rule**? In that case, you should use the conditional disable feature, which you can find right below the Conditional visibility:

![](../../.gitbook/assets/zdfbt.png)

Dive deeper into conditional disable **setup** and **use cases** here:

{% content-ref url="conditional-disable.md" %}
[conditional-disable.md](conditional-disable.md)
{% endcontent-ref %}

Allowing users to add, edit & delete records can be very powerful, but sometimes you want to restrict this to only certain Pages or Teams/Users. With conditional add, edit & delete you can do this:

{% content-ref url="conditional-add-edit-and-delete.md" %}
[conditional-add-edit-and-delete.md](conditional-add-edit-and-delete.md)
{% endcontent-ref %}

