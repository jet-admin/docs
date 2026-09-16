# Field types and primary keys

Each Jet Database table contains records identified by a primary key. The **id** field uniquely identifies each record and cannot be changed or deleted.

## Choose fields for your data

Use a text field for names, a number field for amounts, and a date field for dates. Use the [Field types reference](../data/fields/field-types.md) for other display options.

To extend a table, select **Add field** and choose the appropriate option. See [Add and configure fields](../data/fields/add-and-configure-fields.md).

## Link records with IDs

Store the related record's identifier in a field such as `customer_id`. Configure the relationship using [Link related records](../data/relationships/link-records-across-tables.md). Keep a source system's identifier in its own field when importing data; do not assume it is interchangeable with the Jet Database primary key.

## Verify

Check that each record has an identifier and that a related ID resolves to the intended record. Test with two customers that have different IDs, including any duplicate display names.
