---
description: Learn about the different values types you can work with.
---

# Extract & Pass Values

<figure><img src="../../.gitbook/assets/visual.jpg" alt=""><figcaption></figcaption></figure>

Jet allows you to extract values from **`Visual Builder`**, **`Data`**, and **`Workflow`**. There are the following Values Types:

* Visual Builder/Data/Workflow Values

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

* User and Team Values (Email, First and Last name, token, user id, )

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

* Computed Values (Transform your values with Formula or JavaScript)

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

{% content-ref url="../computed-columns/formulas/" %}
[formulas](../computed-columns/formulas/)
{% endcontent-ref %}

<figure><img src="../../.gitbook/assets/js1.jpg" alt=""><figcaption></figcaption></figure>

{% content-ref url="../computed-columns/javascript-column.md" %}
[javascript-column.md](../computed-columns/javascript-column.md)
{% endcontent-ref %}

## Visual Builder Values

There are two types of Visual Builder values: Component and Page values

### Component Values

Using Component Values you can pass values such as subject and body to `Send email`, filter a list, or pass data from one page to another. You can specify Values for each [page](../design-and-structure/pages.md) or [component](../design-and-structure/components/). Here we guide you through Values types and how to specify Values for a page or component.

![](../../.gitbook/assets/testgif44.gif)

### Page Values

In the case where you want to create a Detail page with information about the user on that page: name, last name, address, etc. You need to pass the parameter values of these fields from one page to another. To do this, you need to create parameters for this page and pass these parameters to another page using the [Navigate to Page](../design-and-structure/actions.md) action.

#### Create Page Values

To create Page Values go to the page settings then click **+Add Parameter.**

![](../../.gitbook/assets/testgif24.gif)

#### Link pages

In order to pass a value from one page to another, you need to use the Navigate to page action.

![](../../.gitbook/assets/testgif25.gif)

{% content-ref url="../design-and-structure/column-values.md" %}
[column-values.md](../design-and-structure/column-values.md)
{% endcontent-ref %}

{% content-ref url="../computed-columns/formulas/" %}
[formulas](../computed-columns/formulas/)
{% endcontent-ref %}

