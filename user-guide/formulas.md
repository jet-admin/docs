---
description: >-
  Formulas may involve functions, numeric operations, logical operations, and
  text operations that operate on fields
---

# Formula

A formula is a method to access every piece of data and build up to as complicated a data flow pattern as you need it to be. You can combine, modify or calculate the values, or you can even pull up an access control system based on logical conditions set by an appropriate formula.

![](../.gitbook/assets/testgif46.gif)

### Basic Math Operations

In a formula, you can reference columns by name and use these to do mathematical calculations. For example, if you wanted a formula that calculated the total based on the price and quantity, the formula would look like:

```
= Price * Quantity
```

### Functions in Formulas

Jet Admin also has a number of useful functions that you can use in your formulas.

**A key thing to remember when using functions is that **_**a message will appear that shows you exactly how to use each function when you click on it.**_ This way, you never have to remember or think about how to use a given formula, you can simply read how to use it and enter or choose the values you need from the menu. \


There are four different groups of built-in functions:

* General Functions – e.g. CONCAT(), IS\_NULL(), LOWER()
* Logical Functions – e.g. IF(), EQ(), AND()
* Mathematical Functions – e.g. ROUND(), ABS(), SUM()
* Date & Time Functions – e.g. NOW(), MONTH(), IS\_DATE\_AFTER()

**Simple Example:**\
You have a table where _First Name_ and _Last Name_ are separate fields, but you would like to concatenate them to display them in one field.

1. Select your table, and then click on _Add computed Column_ in the component menu.
2. Click on the _ƒx Formula_ button next to the value field.
3. Select or search for the CONCAT() function in the menu that appears.
4. Enter the values that you want to concatenate. Like the message shows when you select CONCAT(), the appropriate syntax is CONCAT(_VALUE1,_ _VALUE2_). _VALUE1_ and _VALUE2_ can be fields in your table, or they can be something else (e.g. a string in quotes: "string" – this might be useful for adding a space between table values). For this example, the final result will look like this:

```
=CONCAT(first_name, " ", last_name)
```

<figure><img src="../.gitbook/assets/Untitled16 (1).gif" alt=""><figcaption></figcaption></figure>

Let's see how you can make use of Jet Admin formulas.

### Setting up promotional email

For an introductory example, we will consider feeding customers email addresses to promotional email. Once the user is selected in the Customers table, his or her email should appear in the `Email` field so that to send a promotional Email with a Marketing tool. We will use Functions as well to create a Promotional Email template. For this purpose, we should be performing the following tasks:

1\. Click on Value text area. There will be a pop-up window. Then select Customers table  -> Clicked row (the value will pass once you click a row) -> User email. The Value field will be populated with the following expression:

`=elements.Customers["0"].selected_item.email`

![](../.gitbook/assets/testgif47.gif)

2\. Now we will configure the Subject field using the `CONCAT` function. Let's say we want to select an appropriate value from the Discount dropdown list and have it automatically passed to the Subject field of the promotional email in the following form: "Manuel Allen - 15% discount":

`=CONCAT(elements.Customers["0"].selected_item.username, " - ", elements["Discount"].value)`

![](../.gitbook/assets/testgif48.gif)

3\. To finish up, we shall configure the Body field. Using the `CONCAT` function we will build a template for the email body:

`=CONCAT("Hi ", elements.Customers["0"].selected_item.first_name, ", here is your promocode: ACX978DF.")`

![](../.gitbook/assets/testgif50.gif)

4\. Now when you select any customer, it will launch a completely automated process to create a promotional email to treat this customer. The only manual job remaining for you will be to select the discount and hit the Send email button:

![](../.gitbook/assets/testgif51.gif)

### Create Custom fields using Formulas

In this use case we will create a custom column in the Customer table and calculate a score depends on some logical condition.

1\. Simply create a new Custom field in columns settings of table component.&#x20;

![](../.gitbook/assets/testgif52.gif)

2\. Now we should configure Value for that Column using Formulas. We will use `IF` function to calculate Scores value, depending on Activities number for each customer:

`=IF(item.activities < 280, '50 points', IF(item.activities < 400, '70 points', '100 points'))`

![](../.gitbook/assets/testgif53.gif)

### Formulas variables

Essentially, this is a tabbed pop-up window which reflects all the components on the current page, a list of functions and a set of filters to manage data in the selected table.&#x20;

The number and type of tabs depends on the context. This allows the user to have access to only those tools which are applicable to the objects he or she is working with. For example, if we work with table parameters, there will be a tab with filters. In case we drill down to a specific record of a table and have this record fields displayed on a page, a tab with Record components will be available:

![](../.gitbook/assets/testgif46.gif)

### Tabs context

When you configure the table parameters, the features displayed in the Formulas window will fit the component context, e.g. there will be a new tab with `Filters` to set up filtering for selected table or a tab with [User properties](security-and-privacy/user-and-team-properties.md) if any exists. Let's walk through the possible context Tabs.

#### Search tab

In this tab you see a general list of all available interactions with the current component or other components and parameters.&#x20;

![](../.gitbook/assets/testgif54.gif)

#### Current component tab

When you are working on a Current Component setting, the context in the formulas will show you the Current Component setting at the very top. In this tab, you can only access the fields in the current component:

![](../.gitbook/assets/testgif55.gif)

#### Components tab

Here you can access any data from your resources through any component (fields, tables, charts, etc.) on the current page.

![](../.gitbook/assets/testgif56.gif)

### User-specific properties

If you want to restrict access for a User or a Team to data that is relevant for their work within a JetAdmin app, you can quickly access the [User & Team properties](security-and-privacy/user-and-team-properties.md) in these tabs and assign the user or team ID to the data columns which should be visible for them:&#x20;

![](../.gitbook/assets/testgif57.gif)

You can create custom columns in a table to handle cases such as math operations on your data, parsing JSON fields, or creating conditions. Let's look at a few examples of how to use it:

#### App and Environment properties

Use App name and Environment name properties in your Application to filter your data.

&#x20;![](../.gitbook/assets/app1.jpg)



