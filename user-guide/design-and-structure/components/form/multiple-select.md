---
description: In this section you will learn how to use Multiple Select
---

# Multiple Select

One common type of form is Multiple Select. Multiple Select is useful for when you want auser to be able to select multiple values. This has many applications for an app, but one common use case is using Multiple Select to filter records in a table.

{% embed url="https://youtu.be/XBEyfQF_odY" %}

## Filtering tables with Multiple Select

To use a Multiple Select component as a filter, you need to do two things:

1. Create the Multiple Select form
2. Connect the Multiple Select form to your table as a filter

### Create the Multiple Select form

Once you've dragged and dropped the Multiple Select component into your app, click on it, and the Multiple Select component will appear on the right.

<figure><img src="../../../../.gitbook/assets/Снимок экрана 2023-03-10 в 07.31.32.png" alt=""><figcaption><p>Multiple Select menu</p></figcaption></figure>

Now, you need to set up the options that your user will be able to choose from. You can do this by specifying the options manually or by loading the options.

<figure><img src="../../../../.gitbook/assets/image 360.png" alt=""><figcaption><p>Specify options manually</p></figcaption></figure>

To load the options, first choose the resource and collection that you want to load options from, choose the fields in that collection that you want to use for your labels and values, and then click _Load and customize options_. You can also add subtitles or icons that would then appear in the Multiple Select component.

<figure><img src="../../../../.gitbook/assets/Frame 440.png" alt=""><figcaption><p>Load options</p></figcaption></figure>

After loading the options, be sure to double-check that they are correct and make any changes as necessary. Sometimes extra values will be added, but you can click on the delete icon next to them   to ensure that the list of options is correct.

<figure><img src="../../../../.gitbook/assets/Frame 441.png" alt=""><figcaption><p>Correct options</p></figcaption></figure>

At this point, my Multiple Select component is set up, but I still need to connect it to my table as a filter.

### Connect the Multiple Select form to your table as a filter

Click on your table to open up the table menu on the right. Click on _Filter_, and then in the _Apply Filters_ section, click on _Add._ Next, select the field that you want to filter by, and how you want it to filter. For Multiple Select, it is most common to choose the _\[field] is one of_ option, but depending on your needs, you might also choose _exclude \[field] is one of_.

<figure><img src="../../../../.gitbook/assets/Frame 442.png" alt=""><figcaption><p>Add filter to table</p></figcaption></figure>

The final step is to click on the _ƒx Formula_ button and choose the Multiple Select component from the menu.

<figure><img src="../../../../.gitbook/assets/Frame 443.png" alt=""><figcaption><p>Connect filter to Multiple Select</p></figcaption></figure>



