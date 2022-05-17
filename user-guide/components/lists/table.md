# Table

### Table component

Use `Table` component to view and interact with data from your collections:

![](<../../../.gitbook/assets/image (797).png>)

### Adding Table&#x20;

Adding components explained [here](./#adding-list-component).&#x20;

### Table Settings

You can customize any component in Jet Admin and the Table component is not an exception. You can rearrange columns and enable/disable them:

![](../../../.gitbook/assets/Components5.gif)

On top of it, you can customize each field individually, for example, change the name of a column or change the field type:

![](../../../.gitbook/assets/Components7.gif)

### Search

You can enable Search for your table, just enable the flag:

![](../../../.gitbook/assets/Components8.gif)

### Selection function

Any `table` in Jet Admin has the `selected row` function that can be used to trigger all sorts of actions as well as fetching values from selected records:

![](../../../.gitbook/assets/Components6.gif)

## Actions

Table is an interactive component which means you can bind all **different kinds of actions** to it. You can configure:

* Row click
* Rows check
* Inline action
* Header action
* Hover action

To proceed to the actions, select the table and click on the **"Actions" tab**:

![](../../../.gitbook/assets/dxnrtfyg.png)

{% hint style="warning" %}
For the **Hover action**, you'll need to drill down into an individual column in the column settings (see the "Hover action" section below)
{% endhint %}

### Row click

When the Row click action is enabled, the specified action will be executed once a row is clicked. You'll be able to use any value from a selected row in the action. Now, click on it:&#x20;

![](../../../.gitbook/assets/xhctf.png)

The most **common use-case** for the "Row click" action is drilling down into the record or proceeding to the page with more record-related data (you'll need the "Navigate to Page" action type for that). But you are free to use any action type.

{% hint style="info" %}
Learn more about different types of actions in the [Types of action](../../design-and-structure/actions.md) section
{% endhint %}

![](../../../.gitbook/assets/xftgyju.png)

Here's an **example** of how that might look in the user-mode:

![](../../../.gitbook/assets/tfhyu.gif)

{% hint style="danger" %}
**It's crucial** to understand how **data is bound** under the hood when linking pages. Otherwise, things might break when customizing the auto-generated pages or building the drill-downs from scratch.&#x20;

Please, **read more** in the [Values section](../../parameters/)&#x20;
{% endhint %}



{% hint style="info" %}
When you connect SQL DBs, Firebase, Airtable, or Sheets, Jet Admin automatically generates all the **CRUD** actions - just select them from the dropdown
{% endhint %}

{% content-ref url="./" %}
[.](./)
{% endcontent-ref %}

{% content-ref url="../../design-and-structure/actions.md" %}
[actions.md](../../design-and-structure/actions.md)
{% endcontent-ref %}
