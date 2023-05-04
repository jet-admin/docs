---
description: >-
  Components are UI elements inside Jet Admin that can be used to visualize and
  interact with your data
---

# Components

## Table Editing <a href="#h_d8d3738d09" id="h_d8d3738d09"></a>

Enable users to edit records simply by clicking on a cell in a table. You can even specify which fields you want to make editable. Add table editing to your app for a smoother, intuitive user experience.

<figure><img src="../../.gitbook/assets/table_editing.gif" alt=""><figcaption></figcaption></figure>

## Tooltips <a href="#h_af590998f2" id="h_af590998f2"></a>

Add tooltips to your app components to help new users! Custom tooltips are an unobstrusive way to provide necessary information about how your app functions.

<figure><img src="../../.gitbook/assets/tooltips.gif" alt=""><figcaption></figcaption></figure>

## _On Change_ Field Action <a href="#h_2a04e1f31b" id="h_2a04e1f31b"></a>

Set actions that trigger when a field is updated. This can be great for showing notifications, for quickly setting variables used elsewhere in your app, and for other things as needed.

<figure><img src="../../.gitbook/assets/onchange.gif" alt=""><figcaption></figcaption></figure>

### Setting the Layout

**Layout** components allow you to assemble other components on the page. We recommend starting with the `columns` component - just drag-and-drop it on the page:

![](../../.gitbook/assets/Components3.gif)

### Adding Components

You can add any component by simply drag-and-droping it onto the page:

![](../../.gitbook/assets/Components1.gif)

### Configuring Components

Different components have different settings, which you can access on the right of the window after clicking on the component once. Depending on the component, the menu will have the tabs **General**, **Display**, and **Actions.**

**General:** Contains options for configuring the way the component works. For example: which fields should be included in a table or which datasets to use in a chart.

**Display:** Has display options. For example: **Conditional Visibility**, **Tooltips**, **Component Title**, **Enable Editing** for tables, and whether a field is **Required**.&#x20;

**Actions:** Contains settings for triggering actions based on user interaction with the component. For example: Triggering actions when button is clicked, triggering actions when data is changed.

![](../../.gitbook/assets/Components10.gif)

{% hint style="success" %}
Look at this quick overview of the most commonly used components:
{% endhint %}

### Lists

Lists are UI components used for displaying your collections. You can display your data as `Table`, `Kanban`, `Map`, `Calendar`, `Gallery`, and `Timeline`.

![](<../../.gitbook/assets/image (795).png>)

{% content-ref url="lists/" %}
[lists](lists/)
{% endcontent-ref %}

### Charts

`Charts` let you display your data in several ways: **line**, **bar**, **pie,** **doughnut**, and **single value**.

![](<../../.gitbook/assets/image (798).png>)

![](<../../.gitbook/assets/image (796).png>)

{% content-ref url="charts/" %}
[charts](charts/)
{% endcontent-ref %}

### Text

To set descriptions, you can set different static text elements:

![](<../../.gitbook/assets/image (860).png>)

{% content-ref url="text.md" %}
[text.md](text.md)
{% endcontent-ref %}

### Media & Files

You can use images, files, and videos in Jet Admin. Just drag-and-drop the right component and configure it:

![](../../.gitbook/assets/Components2.gif)

### Buttons

Buttons are used to execute actions. For example, you can create buttons to execute: Copy to clipboard, Send an email, Open a link, Link to page, and others.

![](<../../.gitbook/assets/image (861).png>)

{% content-ref url="buttons.md" %}
[buttons.md](buttons.md)
{% endcontent-ref %}

### Forms

Forms are the UI elements that are used to receive or display single values. They can be set as editable or non-editable.

![](../../.gitbook/assets/Components4.gif)

{% content-ref url="../design-and-structure/components/form/" %}
[form](../design-and-structure/components/form/)
{% endcontent-ref %}

### Custom component

It is a Component based on React, Angular, or any other framework and integrates it in Jet Admin interface.

{% content-ref url="custom-component.md" %}
[custom-component.md](custom-component.md)
{% endcontent-ref %}
