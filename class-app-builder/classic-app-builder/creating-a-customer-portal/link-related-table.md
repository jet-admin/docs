---
description: >-
  In this section you will learn how to link related tables for creating a
  customer portal
---

# Link Related Tables

You can **link different tables** as long as there's a common field in both of them. In our case, we'll link by the `Unit name` field.

{% hint style="info" %}
In Jet Admin you can link tables from **different Bases**
{% endhint %}

### Display the Projects

Drag the `Table` component and change the mock data to your own. Select the data source you've connected and the page you want to display:

1. Drag and Drop the Table Component to the page
2. Choose the Resource and the Collection

{% @arcade/embed flowId="7q2aksuonDvNDmR9Ybem" url="https://app.arcade.software/share/7q2aksuonDvNDmR9Ybem" %}

### Link the Tables

Each `Unit` has many `Tasks` and we want to see the list of `Tasks` for a given `Unit`. To create this flow, follow the steps:

1. Click on the T**able**
2. Click on the `Filter` icon
3. Choose **Unit ID -> ID equals**
4. Click on the `Formula` icon&#x20;
5. Choose **Units -> Selected Row -> ID**

{% @arcade/embed flowId="hdBNu4urzBykb3PXvuFR" url="https://app.arcade.software/share/hdBNu4urzBykb3PXvuFR" %}

Now, let's **customize** our Portal:

{% content-ref url="customize-your-portal.md" %}
[customize-your-portal.md](customize-your-portal.md)
{% endcontent-ref %}
