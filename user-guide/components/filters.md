# Filters

This UI component allows you to add a filter as a standalone building block and use it anywhere on a page. There is a [separate filter built-in](https://docs.jetadmin.io/user-guide/design-and-structure/filter) that is included on all tables.

{% hint style="warning" %}
The filter component is for single tables and is not for charts or for use with multiple UI components at once.
{% endhint %}

You can find filters in the UI building block library inside of the Builder.

<figure><img src="../../.gitbook/assets/Group 764.png" alt=""><figcaption></figcaption></figure>

After you place it on the canvas, there are a few steps to make it work:

#### 1. Bind to a component

Bind a filter to the UI component that you want to be filtered. For this, click on the "Bind to component" button **(1)** and choose the Ui component from the list **(2)**

<figure><img src="../../.gitbook/assets/Group 766.png" alt=""><figcaption></figcaption></figure>

#### 2. Create a filter

Then add a filter, choosing the field by which you want the data in the UI component to be filtered and the logical expression, for example "greater than."

<figure><img src="../../.gitbook/assets/Снимок экрана 2023-03-16 в 08.42.29.png" alt=""><figcaption></figcaption></figure>

3\. Filter is ready

Now you can preview and test your filter. You can add multiple filters; in a one filter component, each filter will function with logical AND between them. This means that, in the example below, only records that have both a status of _Active_ AND an _Enterprise_ plan will be shown in the table. &#x20;

<figure><img src="../../.gitbook/assets/Снимок экрана 2023-03-16 в 08.45.59.png" alt=""><figcaption></figcaption></figure>

