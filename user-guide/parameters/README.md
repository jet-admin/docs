---
description: >-
  When we configure our app, we're constantly working with values and using them
  in different ways.
---

# 🔗 Binding & Values

{% embed url="https://www.youtube.com/watch?v=r0yL_CQh9J8&ab_channel=JetAdmin" %}

Your business data in Jet Admin apps are surfaced with components. Depending on the granularity level, a [component](https://app.gitbook.com/@jetadmin/s/doc/\~/drafts/-MijlldWuqWYchvMUiLt/user-guide/components) can range from a table to a field in a table.‌

## Component Values

Using Values you can pass values such as subject and body to `Send email`, filter a list, or pass data from one page to another. You can specify Values for each [page](../../getting-started/quickstart/set-the-layout.md) or [component](../components/). Here we guide you through Values types and how to specify Values for a page or component.

![](../../.gitbook/assets/testgif44.gif)

## Page Values

In the case where you want to create a Detail page with information about the user on that page: name, last name, address, etc. You need to pass the parameter values of these fields from one page to another. To do this, you need to create parameters for this page and pass these parameters to another page using the [Navigate to Page](../design-and-structure/actions.md) action.

### Create Page Values

To create Page Values go to the page settings then click **+Add Parameter.**

![](../../.gitbook/assets/testgif24.gif)

### Link pages

In order to pass a value from one page to another, you need to use the Navigate to page action.

![](../../.gitbook/assets/testgif25.gif)

{% content-ref url="column-values.md" %}
[column-values.md](column-values.md)
{% endcontent-ref %}

{% content-ref url="../formulas.md" %}
[formulas.md](../formulas.md)
{% endcontent-ref %}

