# Single relations

**Single relations** help you fetch data from the **related collections**.&#x20;

To illustrate how it works, let's imagine we have the `Transactions` table that doesn't contain a **customer's email** and the `Users` table that contains the customer information including the email:

![](<../../.gitbook/assets/image (874).png>)

And we want to **display the email** in the `Transactions` list:

![](<../../.gitbook/assets/image (875).png>)

First of all, we identify how our tables are **related**: for each user, there are several transactions that are related to the users list by the **ID** and **Customer ID fields:**

![](../../.gitbook/assets/sdhx.PNG)

Now, let's create a new **custom column** in the `Transactions` table:

![](../../.gitbook/assets/deep1.gif)

Then change the **column type** to `Link to record`

![](../../.gitbook/assets/deep2.gif)

Now, we need to select where we'll get the user email from (a related `Users` table), what field in the `Users` table is used to set relations with the `Transactions` table (the `ID` field), and what field from the `Users` table we'd like to display (the `Email` field):

![](../../.gitbook/assets/deep3.gif)

And the **final step** is to get our custom field value from the `Transactions` table field that sets relations to the `Users` table (the `Customer ID` field):

![](../../.gitbook/assets/deep4.gif)

Now, let's make UI components **dynamically visible** based on a rule:

{% content-ref url="conditional-visibility.md" %}
[conditional-visibility.md](conditional-visibility.md)
{% endcontent-ref %}
