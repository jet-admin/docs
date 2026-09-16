# Connect a table to an edit form

Applies to **Classic App Builder**. Screens and recordings in this section show the Classic interface.

Show the selected table record in a form, then update that specific record.

**Before you start:** prepare a table and form for the intended resource, a stable record identifier, and two distinguishable synthetic records.

## Configure the data flow

1. Connect the table to the intended collection.
2. Select a test row.
3. In the form or its field settings, use the available **Bind** or **Functions** control to reference values from the table's selected record.
4. Match each source field to the corresponding form input.
5. Configure the submission operation to update the selected record, using its stable identifier and the form's editable values.
6. Configure any required post-submit refresh through the relevant component action.

![Classic binding example showing a selected table value referenced by an input](<../../.gitbook/assets/image (4) (3) (1).png>)

The screenshot illustrates the binding principle; the form and operation controls depend on the component you use. See [Binding components](binding-components.md) and [Actions](../actions-and-logic/actions.md) for the controls.

## Verify the result

Select record A, then record B: the form should follow the selection. Change one field on B, submit, and verify that only B changed in the source. Test an empty selection and a user who cannot update the record.

If the wrong record changes, inspect the identifier passed to the update operation before changing the display binding.

## Existing Classic video

{% embed url="https://www.youtube.com/watch?v=rdM-p_fgi-k" %}
