# Connect a filter to a table

Applies to **Classic App Builder**. Screens and recordings in this section show the Classic interface.

Use a filter component's value to control which records a table displays.

**Before you start:** prepare a table, a filter/input component, and synthetic records with at least two different values for the field you will filter.

## Configure the binding

1. Connect the table to the intended collection.
2. Identify the filter component's output value.
3. In the table's filter configuration, choose the field and comparison required by your use case.
4. Bind the comparison value to the filter component's output using the available value picker.
5. Check that the input and field types match.
6. Preview the page and change the filter value.

![Classic Functions value picker used to reference a component value](<../../.gitbook/assets/image (1) (1) (1) (1) (2).png>)

For the general value-selection workflow, see [Binding components](binding-components.md). For compound conditions, see [Nested filters](../design-and-structure/nested-filters.md).

## Verify the result

Test a matching value, a different matching value, no matches, and an empty input. Define whether clearing the filter should show all permitted records or another explicit result.

If nothing changes, inspect the referenced component and its output. If results are unexpected, check the comparison, value type, and other active filters.

A display filter is not proof of record authorization. For restricted data, test [record access](../../access-and-sharing/app-and-data-permissions/record-access.md) independently.

## Existing Classic video

{% embed url="https://www.youtube.com/watch?v=zZxiLuhdiGI" %}
