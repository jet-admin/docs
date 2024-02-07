# Table

### Table component

Use `Table` component to view and interact with data from your collections:

![](<../../../../../.gitbook/assets/image (797).png>)

### Adding Table&#x20;

Adding components explained [here](../../../../components/lists/#adding-list-component).&#x20;

### Table Settings

You can customize any component in Jet Admin and the Table component is not an exception. You can rearrange columns and enable/disable them:

![](../../../../../.gitbook/assets/Components5.gif)

On top of it, you can customize each field individually, for example, change the name of a column or change the field type:

![](../../../../../.gitbook/assets/Components7.gif)

### Search

You can enable Search for your table, just enable the flag:

![](../../../../../.gitbook/assets/Components8.gif)



### Selection function

Any `table` in Jet Admin has the `selected row` function that can be used to trigger all sorts of actions as well as fetching values from selected records:

![](../../../../../.gitbook/assets/Components6.gif)

### Grouping Rows in Tables

Jet Admin lets you group table rows together to better organize your data.\
To do this, go to the Display section and scroll down to 'Group By'.

<figure><img src="../../../../../.gitbook/assets/group by 2 (1).gif" alt=""><figcaption></figcaption></figure>

Choose the field to group rows by, enter a label for each group, and pick a color to highlight the groups.\
\


<figure><img src="../../../../../.gitbook/assets/group by 3 (1).gif" alt=""><figcaption></figcaption></figure>

### Grouping Rows in Tables

Jet Admin lets you group table rows together to better organize your data.

To do this, go to the Display section and scroll down to 'Group By'.

<figure><img src="../../../../../.gitbook/assets/group by 2.gif" alt=""><figcaption></figcaption></figure>

Choose the field to group rows by, enter a label for each group, and pick a color to highlight the groups.

<figure><img src="../../../../../.gitbook/assets/group by 3.gif" alt=""><figcaption></figcaption></figure>

### Hiding Filters from Filter

Hiding fields lets you only show preferred filters in the list.

Go to 'Display Filters' and you can disable all filters, which removes the filter icon completely.

Or choose to hide some filters by clicking the toggle button next to each one.

<figure><img src="../../../../../.gitbook/assets/filter 1.gif" alt=""><figcaption></figcaption></figure>

### Statically Filter Data Using JavaScript

To filter your data statically in a table with more than one value, in this case we need to use JavaScript.

For example, if we have data with different statuses (New, Started, Blocked, and Completed). And we need to show data only with statuses "Blocked" and "Completed".

First we need to choose a column to filter by then use the filter "one of"

<div align="left">

<figure><img src="https://downloads.intercomcdn.com/i/o/909279041/17636c48766584c0229a5eba/image.png?expires=1702553288&#x26;signature=8351b93cdfcdd53a9acde96ecf6fe98b0b70a2ea06468ee38a09841af187d4be" alt=""><figcaption></figcaption></figure>

</div>

Then activate the formula

<div align="left">

<figure><img src="https://downloads.intercomcdn.com/i/o/909281433/b5b998cd50948133f02cdfe2/image.png?expires=1702553288&#x26;signature=8854516eab49a6add501ba1637873b7a05970b7ff1dc49705f91f106765cc96c" alt=""><figcaption></figcaption></figure>

</div>

Then click on the **JavaScript** button, and  type the code below:

```
let arr = ["Blocked","Complete"]; 
return arr;
```

{% hint style="info" %}
Values inside the JavaScript code are case sensitive. beware of the capital and small litters&#x20;
{% endhint %}

This will result to showing only records with statuses "Blocked" and "Started" as shown in the image below:\
​

<figure><img src="https://downloads.intercomcdn.com/i/o/909285595/2d526ecc6671ccacc1122646/image.png?expires=1702553288&#x26;signature=9ebbb8aaf1ca254d3b64dfad996464cf1d6344dbd839de2e7ab597eec010791e" alt=""><figcaption></figcaption></figure>

​\
​\
​\
​

\
​

##
