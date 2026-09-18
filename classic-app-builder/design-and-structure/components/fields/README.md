---
description: Fields overview
icon: i-cursor
---

# Fields

Applies to **Classic App Builder**. These controls configure how a field is displayed in a component; changing its presentation is different from changing the source schema.

Fields are single record data obtained from your resources. By default, all fields from your resource will be rendered as a text, but you can switch to a more appropriate one.

For example, you have a table of your customer's details, you can click on a record to see all available fields. All records from the same collection share the same fields. For example, each customer will have a specific `Firstname`, `Lastname`, `Email`.

![](<../../../../.gitbook/assets/GIF (282).gif>)

### Customize your fields

Your fields are what contains your data. They belong to a collection, so in order to customize them, go to Visual Builder and choose which field you will customize.

![](<../../../../.gitbook/assets/GIF (283).gif>)

### Field Types

By default, all fields from your resource will be rendered as a text - this is the most basic way to display your content (depending on your field type). But if you need to change your field type, you can set it up manually. For example, use a numeric presentation for quantities. Keep phone numbers as text so that leading zeros, country prefixes, and formatting are preserved.

![](<../../../../.gitbook/assets/image (6).gif>)

### Field Data

You can get the value of the selected record in the component by configuring the parameter transfer. For example, you want to display the `email` of the selected user.

![](<../../../../.gitbook/assets/image (14).gif>)

### Bind a field to a selected record

See [Binding Field to Table](../../../binding-and-values/binding-field-to-table.md) to display a value from the selected row, and [Field types](../../../../user-guide/data/fields/field-types.md) for source-data considerations.

Test two different records and an empty value to confirm the displayed field follows the selection. The retained images show the earlier Classic interface.
