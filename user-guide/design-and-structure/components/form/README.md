---
description: In this section you will learn how to use Forms
---

# Form

Submit a **Form** to perform actions with input data. The Form component provides a way for users to view and manipulate multiple data fields with their inputs. Upon submission, forms perform functions like creating (inserting) a new data record, updating an existing record, or [calling APIs](../../../data/make-an-http-request.md).

{% embed url="https://vimeo.com/817555123" %}

Use a form if you expect the user to interact with multiple data fields for the form's function. If you need a user to enter an email and customer name, select an item from a dropdown, and then write a paragraph of text, forms are your best option. This is usually the best component when your function is to create entirely new data records.

![](<../../../../.gitbook/assets/image (876).png>)

{% hint style="success" %}
You’re looking to build a tool to allow your business to take new orders over the phone. The tool will need to record the **customer name**, **phone number**, **address**, **product SKU**, and **payment information**, and store it in your **Orders** table in your database.

Because there are multiple fields with user input, you choose to use a **Form**. For fields like the **name** and **address**, you allow the user to type in the text. For the **Product SKU** and **Payment** **Type**, you set up a dropdown selector ("Visa", "Mastercard", etc). When submitted, the form inserts a new Order record with this data into your database.
{% endhint %}

### Create Form

To add a Form, simply drag and drop the Form component to the page and then choose the resource and collection for which you want to generate the form.

{% content-ref url="create-a-form.md" %}
[create-a-form.md](create-a-form.md)
{% endcontent-ref %}

{% hint style="info" %}
Now, when you fill out the form, you will be able to create a new record in your database.
{% endhint %}

### Customize the Form view

You can customize the form's appearance, such as arranging fields horizontally in multiple columns.&#x20;

{% content-ref url="customize-a-form-view.md" %}
[customize-a-form-view.md](customize-a-form-view.md)
{% endcontent-ref %}

### Examples

Please see some examples and use cases of Forms in the article:

{% content-ref url="examples.md" %}
[examples.md](examples.md)
{% endcontent-ref %}

### Multiple Select

One common type of form is Multiple Select. Multiple Select is useful when you want a user to be able to select multiple values. This has many applications for an app, but one common use case is using Multiple Select to filter records in a table.

{% content-ref url="multiple-select.md" %}
[multiple-select.md](multiple-select.md)
{% endcontent-ref %}
