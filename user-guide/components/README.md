---
description: >-
  Components are UI elements inside Jet Admin that can be used to visualize and
  interact with your data
---

# Components

## Table Editing <a href="#h_d8d3738d09" id="h_d8d3738d09"></a>

Enable users to edit records simply by clicking on a cell in a table. You can even specify which fields you want to make editable. Add table editing to your app for a smoother, intuitive user experience.

To make a field editable, follow the steps:

1. Click on the **Table**
2. Go to the `Display` Tab
3. Go to the `Editable` Tab
4. Click on the **Settings** icon
5. Make Email **Non-editable**

{% @arcade/embed flowId="pjRtS7zUZZ7ZInwx6UFy" url="https://app.arcade.software/share/pjRtS7zUZZ7ZInwx6UFy" %}

## Tooltips <a href="#h_af590998f2" id="h_af590998f2"></a>

Add tooltips to your app components to help new users! Custom tooltips are an unobtrusive way to provide necessary information about how your app functions.

Let's add a tooltip for the button. Follow the steps,

1. Click on the `Button`
2. Go to the Display Tab
3. Scroll down to the Tooltip Section
4. Specify the tooltip

{% @arcade/embed flowId="NCzdTRnpTh2HtBObbK2L" url="https://app.arcade.software/share/NCzdTRnpTh2HtBObbK2L" %}

## _On Change_ Field Action <a href="#h_2a04e1f31b" id="h_2a04e1f31b"></a>

Set actions that trigger when a field is updated. This can be great for showing notifications, for quickly setting variables used elsewhere in your app, and for other things as needed.

1. Click on the **Text Field**
2. Go to the `Actions` Tab
3. Click on the `Value Changes`
4. Choose `Show Notification`
5. Specify the `Title` by using **Formula**
6. Set it to the `Value`

{% @arcade/embed flowId="8rwb4y02rYu6Oh306hmV" url="https://app.arcade.software/share/8rwb4y02rYu6Oh306hmV" %}

## Setting the Layout

**Layout** components allow you to assemble other components on the page. We recommend starting with the `columns` component - just drag and drop it on the page. Let's create one together.

Follow the steps:

1. Drag and Drop **Columns** to the Page
2. Add a **Container** to each of the Column
3. Add a **Column** to the First Column
4. Add **Tabs** to the second Container

{% @arcade/embed flowId="jY5WwokSRbtAp4zDiSGQ" url="https://app.arcade.software/share/jY5WwokSRbtAp4zDiSGQ" %}

### Adding Components

You can add any component by simply dragging and dropping it onto the page. Let's add the Table and Details component to the Layout. Follow the steps:

1. Drag and Drop the **`Table`** component to the first Container
2. Go to the **All Components**
3. Scroll down to the **Forms Section**
4. Drag and Drop the **`Details`** component to the second Container

{% @arcade/embed flowId="WZVQyEGe3m5qhWt7VVbn" url="https://app.arcade.software/share/WZVQyEGe3m5qhWt7VVbn" %}

### Configuring Components

Different components have different settings, which you can access on the right of the window after clicking on the component once. Depending on the component, the menu will have the tabs **General**, **Display**, and **Actions.**

**General:** Contains options for configuring the way the component works. For example: which fields should be included in a table or which datasets to use in a chart.

**Display:** Has display options. For example, **Conditional Visibility**, **Tooltips**, **Component Titles**, **Enable Editing** for tables, and whether a field is **Required**.&#x20;

**Actions:** Contains settings for triggering actions based on user interaction with the component. For example: Triggering actions when the button is clicked, and triggering actions when data is changed.

To see the tabs:

1. Click on the Component

{% @arcade/embed flowId="SDfyNVD8UYojBDDMCnd4" url="https://app.arcade.software/share/SDfyNVD8UYojBDDMCnd4" %}

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

You can use images, files, and videos in Jet Admin. Just drag and drop the right component and configure it.&#x20;

For adding Media & File Components, follow the steps:

1. Drag and Drop the Image Picker Component on the page
2. Drag and Drop the File Picker Component on the page
3. Drag and Drop the Video Picker Component on the page
4. Drag and Drop the Audio Picker Component on the page

{% @arcade/embed flowId="S1fBrpkbq5hMKalkb9Z3" url="https://app.arcade.software/share/S1fBrpkbq5hMKalkb9Z3" %}

### Buttons

Buttons are used to execute actions. For example, you can create buttons to execute: Copy to a clipboard, Send an email, Open a link, Link to a page, and others.

![](<../../.gitbook/assets/image (861).png>)

{% content-ref url="buttons.md" %}
[buttons.md](buttons.md)
{% endcontent-ref %}

### Forms

Forms are the UI elements that are used to receive or display single values. They can be set as editable or non-editable.

{% content-ref url="../design-and-structure/components/form/" %}
[form](../design-and-structure/components/form/)
{% endcontent-ref %}

### Custom component

It is a Component based on React, Angular, or any other framework and integrates it into the Jet Admin interface.

{% content-ref url="../design-and-structure/components/custom-component/" %}
[custom-component](../design-and-structure/components/custom-component/)
{% endcontent-ref %}
