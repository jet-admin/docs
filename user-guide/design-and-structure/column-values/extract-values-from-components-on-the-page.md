---
description: >-
  In this section you will learn how to extract values from components on the
  page
---

# Extract values from components on the Page

Let's say you have the Customers table. Once the user is selected in the Customers table, his or her email value will be used as the `User email` parameter to send a promotional email with a Marketing tool. The succession of events will be this:

1. Click on the `Value` text area
2. From the pop-up window, select **Customers** table&#x20;
3. Choose the `Selected row` (the value will pass once you click a row)
4. Select the **User's email**

{% @arcade/embed flowId="w9zdRj4SoT8HdIgjEmWM" url="https://app.arcade.software/share/w9zdRj4SoT8HdIgjEmWM" %}

The Value field will be populated with the following expression `=elements.Customers["0"].selected_item.email`

<figure><img src="../../../.gitbook/assets/image (920).png" alt=""><figcaption></figcaption></figure>

### Ask the user to fill out the form in your App

In that case, we need to configure Values for the "Send Email" button.

1. Click on the `Value` text area
2. Select `Ask from user option` in the [Formulas](../../formulas.md) pop-up window.&#x20;

NEEDS TO BE CHANGED-> COULD NOT FIND THE ASK FROM USER OPTION

Now, when the user sends an email, the values will automatically be passed from the selected row in the table to the button values.
