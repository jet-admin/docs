---
description: We'll learn how data binding works inJet Admin
---

# Overview

Once you've connected your Data Sources and dropped relevan UI building blocks on the canvas, it's time to connect the UI and Data to set up the business logic

### What is binding?

If you have, say, a table component on the canvas and you want to display your "Companies" data (collection) in it, it's pretty easy: you go into the table settings and link it to the collection:

<figure><img src="../../.gitbook/assets/image (3) (3).png" alt=""><figcaption></figcaption></figure>

But what if we move up the complexity a bit and would want to mke the `email` value from the selected row **appear in the input field**?

<figure><img src="../../.gitbook/assets/image (4) (3).png" alt=""><figcaption></figcaption></figure>

In this case, we'll need **"Bind"**  (or link) the two componnets - a Table and an Input field. For this, we'll need to reference the email from the selected row in the table from the input field.

{% hint style="info" %}
Jet is designed so that (almost) all the dynamic values, such as values from selected elements, user and team properties, outputs of workflows, or values from HTTP responses are **"available" for referencing** from anywhere in the app
{% endhint %}

### Ways to bind

There are generally two ways how you can bind components in Jet:

* Either through the simplified "Bind" option:

<figure><img src="../../.gitbook/assets/Screenshot (206).png" alt=""><figcaption></figcaption></figure>

* Or through more advanced "Functions" option (where you can transform data and do lots of other cool things)

<figure><img src="../../.gitbook/assets/Screenshot (207).png" alt=""><figcaption></figcaption></figure>

**The Formulas modal** window allows you to find and reference any dynamic value from the UI components, and any parameter from Users, Teams, and API responses. As well as transform values using Excel-like formulas or using JavaScript



<figure><img src="../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

All the components available for referencing are listed in various tabs. Then you can drill down into a component (in our case, it's `Deals` table) and choose the field to reference. This will fetch this value from the component we referenced onto the component we reference from.

<figure><img src="../../.gitbook/assets/dxhtcfvg.gif" alt=""><figcaption></figcaption></figure>

The same logic applies to all the cases where you want to grab one dynamic value and pass it over into some other place to either display or transform or filter by this value.



