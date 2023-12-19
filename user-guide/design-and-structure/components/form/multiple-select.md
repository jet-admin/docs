---
description: In this section you will learn how to use Multiple Select
---

# Multiple Select

One common type of form is Multiple Select. Multiple Select is useful for when you want auser to be able to select multiple values. This has many applications for an app, but one common use case is using Multiple Select to filter records in a table.

{% embed url="https://youtu.be/XBEyfQF_odY" %}

## Filtering tables with Multiple Select

To use a Multiple Select component as a filter, you need to do two things:

1. Create the **Multiple Select** form
2. Connect the **Multiple Select** form to your table as a **filter**

### Create the Multiple Select form

To create a multiple-select form:

1. Drag and drop the Multiple Select component into your app
2. Click on it, and the Multiple Select component will appear on the right.

{% @arcade/embed flowId="NkPPAwWXv3scA7CVwD10" url="https://app.arcade.software/share/NkPPAwWXv3scA7CVwD10" %}

Now, you need to set up the options that your user will be able to choose from. You can do this by specifying the options manually or by loading the options.

To specify options manually, follow the steps:

1. Scroll down and click on the `Add an Option` button
2. Add Options

{% @arcade/embed flowId="UmV76BycmPWRgwRgc3YN" url="https://app.arcade.software/share/UmV76BycmPWRgwRgc3YN" %}

To load the options, follow the steps:

1. Click on the **`Load Options`**
2. Choose the **resource** and **collection** that you want to load options from
3. Choose the **fields** in that collection that you want to use for your **labels** and **values**
4. Click _`Load and Customize` options_. You can also add subtitles or icons that would then appear in the Multiple Select component.

{% @arcade/embed flowId="Ht5hZ33aMWUklti3MkUK" url="https://app.arcade.software/share/Ht5hZ33aMWUklti3MkUK" %}

{% hint style="warning" %}
After loading the options, be sure to double-check that they are correct and make any changes as necessary. Sometimes extra values will be added, but you can click on the delete icon next to them to ensure that the list of options is correct.
{% endhint %}

At this point, my Multiple Select component is set up, but you still need to connect it to my table as a filter.

### Connect the Multiple Select form to your table as a filter

1. Click on your table to open up the table menu on the right.&#x20;
2. Click on _Filter_, and then in the _Apply Filters_ section, click on _Add._&#x20;
3. Next, select the field that you want to filter by, and how you want it to filter. Choose **discount provided** -> **discount provided equals**
4. For Multiple Select, it is most common to choose the _\[field] as one of_ the options, but depending on your needs, you might also choose to _exclude \[field] as one_.

{% @arcade/embed flowId="WeyDt1HTWjypur0jb2dt" url="https://app.arcade.software/share/WeyDt1HTWjypur0jb2dt" %}

