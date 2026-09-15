---
description: >-
  Create a Jet Tables database, choose a template, import a file, and manage
  your data.
icon: database
---

# Jet Databases

Jet Databases gives you a PostgreSQL database hosted by Jet Admin, with a spreadsheet-style interface for working with your data. In the resource picker, it is called **Jet Tables**.

You can edit, search, filter, and sort records; import or export CSV, XLS, XLSX, and JSON files; and query your data with SQL. You can also [combine data from other sources](../synced-tables/) and access your tables through the [API reference](/broken/pages/-M2Ezm-MS-DTMS9hxOtE).

## 1. Open Jet Tables

1. Open your application and select **Data** in the top navigation.
2. Open the data resource menu and select **Add Resource**.
3. In **Create a Resource**, select **New Data — using Jet Tables**.

If you already have a Jet Tables resource, select it from the resource menu to work with its tables.

<figure><img src="../../.gitbook/assets/00-new-data.png" alt="Create a Resource dialog with New Data using Jet Tables as the first option"><figcaption><p>Select New Data to start with Jet Tables.</p></figcaption></figure>

## 2. Create a table

The setup window offers three starting points:

| Option               | Use it to                                                                             |
| -------------------- | ------------------------------------------------------------------------------------- |
| **New Table**        | Start with the default example fields and records, then adapt the table to your data. |
| **Template**         | Start from a Customers, Tasks, Companies, Tickets, or Deals template.                 |
| **Import from File** | Bring in data from an existing file.                                                  |

### Start with New Table

1. Select **New Table**.
2. Use the pencil icon beside the table name to rename it. This walkthrough uses **Documentation Demo**.
3. Review the fields and sample records in the preview.
4. Select **Create** to create the table.

<figure><img src="../../.gitbook/assets/01-new-table.png" alt="New Table setup showing the Documentation Demo name, default fields, and sample records"><figcaption><p>Name your table and review the preview before selecting Create.</p></figcaption></figure>

### Start from a template

Select a template from the left sidebar to preview its fields and sample data. Rename the table if needed, then select **Create**.

<figure><img src="../../.gitbook/assets/02-template.png" alt="Tasks template selected with a preview of its fields and example task records"><figcaption><p>The Tasks template provides a starting structure for tracking work.</p></figcaption></figure>

## 3. Import an existing file

To start with your own data:

1. Select **Import from File** in the setup window.
2. Select **Choose File**, or drag a file into the upload area. Supported formats are **CSV, XLS, XLSX, and JSON**.
3. If needed, open **Advanced settings** to review the encoding and automation settings.
4. Select **Import file**.

<figure><img src="../../.gitbook/assets/03-import-file.png" alt="File import dialog with Choose File, supported formats, Advanced settings, and Import file"><figcaption><p>Upload an existing file to bring your data into Jet Tables.</p></figcaption></figure>

## 4. Work with your table

Once your table is created, use the data workspace to manage its structure and records:

* **Left sidebar:** select and manage your tables.
* **Table toolbar:** open the selected table's structure, field settings, and API options.
* **Data grid:** view and edit records.

<figure><img src="../../.gitbook/assets/table view.png" alt="Jet Tables data workspace showing the table sidebar, toolbar, and records grid"><figcaption><p>The data workspace provides access to tables, fields, and records.</p></figcaption></figure>

Edit the existing fields and add new fields to match the data your application needs.

<figure><img src="../../.gitbook/assets/edit or add field.png" alt="Jet Tables grid showing controls for editing existing fields and adding fields"><figcaption><p>Adapt the table by editing or adding fields.</p></figcaption></figure>

{% hint style="warning" %}
The **id** field is the primary key: it uniquely identifies each record and cannot be changed or deleted.
{% endhint %}

For more about managing records, searching, filtering, and sorting, see the [Data guide](https://docs.jetadmin.io/user-guide/data). To work with records programmatically, see the [API reference](/broken/pages/-M2Ezm-MS-DTMS9hxOtE).

## Video walkthrough

{% embed url="https://www.youtube.com/watch?v=2rdWPCUiGd4&list=PLSkzi9eq0vBnUGMnwXrRRVo9TXUjZ7uSj&index=18&ab_channel=JetAdmin" %}
