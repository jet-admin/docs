# Bind page data to a modal

Applies to **Classic App Builder**. Pass a value from a selected table row into a modal, slideout, or other overlay.

## Example: show the selected product

The page contains a Products table. The modal needs the selected Product ID to display the matching product or initialize a record-specific form.

1. [Create a modal](../design-and-structure/components/modal.md).
2. In **Customize Overlay → Overlay Parameters**, add a parameter for the product identifier. Choose a type compatible with the source field.
3. On the table, configure **Row click → Open Overlay** and choose that modal.
4. Supply the selected row's Product ID to the overlay parameter in the opening action.
5. Inside the modal, bind the receiving component to that parameter. For a Detail component, use it as the primary-key filter.
6. Open two different rows in turn and confirm each shows the matching product.

Use the unique identifier to select the record. Binding an input's initial value alone does not configure a save action.

## Check the binding

* Confirm the source is the currently selected row, not a fixed sample value.
* Match the parameter type to the identifier.
* Check the empty-selection case for a button that opens the modal.
* Test a second record to catch stale values.
* Test any write action separately using synthetic data and the intended user's permissions.

For symptoms and fixes, see [Modal troubleshooting](../design-and-structure/components/modal.md#troubleshooting).

## Classic video walkthrough

This retained recording shows an earlier Classic interface. The text above provides the steps without requiring video playback.

{% embed url="https://www.youtube.com/watch?v=t-93auOdrno&list=PLSkzi9eq0vBnUGMnwXrRRVo9TXUjZ7uSj&index=16&ab_channel=JetAdmin" %}

See [Overlay Parameters](../design-and-structure/components/layouts/overlays/overlay-parameters.md) for the parameter setup walkthrough. Current-interface execution and replacement video production remain pending.
