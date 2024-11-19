---
description: >-
  The export feature allows you to download a set of data to CSV, XLS, XLSX,
  JSON, HTML, and Notepad (txt) formats.
---

# Export

If you are exporting data using a table component, you will be provided two options as data sources. `This Component` and `Set Data Source.` &#x20;

<div align="left">

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

</div>

### This Component

This option allows you to export the current data shown on the table. You will also be able to sort the data based on a specific column. Choose the columns to include, and set the number of records to export.

### Set Data Source

This option provides three options:

* **Load Data:** Load data from a connected data source.
* **Load Using Workflow:** Load data resulting from a workflow.
* **Specify Data**: Load data from another component, page query, or a variable.

You will also be able to sort the data based on a specific column. Choose the columns to include, set the number of records to export, and set filters.

<div align="left" data-full-width="false">

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

</div>

### Export selected row

First, you need to add an export action to the table for exporting selected rows. To do it, follow the steps:

1. Drag-and-drop a  `Table` to your page
2. Go to the **Actions** Tab
3. Click on the `Row Checked` button
4. Click on the **New Action**
5. From the dropdown menu, choose `Export Data`
6. Click on the **Choose Resource**&#x20;
7. Click on the `Add` button to apply a filter
8. To apply a filter, choose **ID equals**
9. Choose the **formula** for the filter

{% @arcade/embed flowId="w0F7I6K8zq7QHO3VMbdZ" url="https://app.arcade.software/share/w0F7I6K8zq7QHO3VMbdZ" %}

### Now, let's test it

1. Click on the **rows** you want to export
2. Click on the `New Action` button
3. Click on the `Execute` button
4. Choose the **format** of the file
5. Choose **CSV** for exporting the file as CSV
6. Click on the `Export` button

{% @arcade/embed flowId="XFq70hOR2pcQlbWWo7bE" url="https://app.arcade.software/share/XFq70hOR2pcQlbWWo7bE" %}

### Rename the button

1. Click on the **Text** field&#x20;
2. Rename the button

{% @arcade/embed flowId="EnAeqhkbd47OhGt2rEDb" url="https://app.arcade.software/share/EnAeqhkbd47OhGt2rEDb" %}
