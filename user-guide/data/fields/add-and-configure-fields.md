# Add and configure fields

Use a stored field for a value you enter, a computed field for a calculation, or a related field for data linked from another table.

## Add a field in Jet Tables

1. Open **Data**, select your Jet Tables resource, and open the table.
2. Select **Add field** at the right end of the column headers.
3. Choose **Add new field**.
4. Set the name and a type that matches the values you will store, then complete the field configuration.
5. Enter a sample value in a test record. Reopen it and confirm that the value and format are correct.

<figure><img src="https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2FnD8tpnrXT4Kc91tmSHGw%2F06-ticket-fields.png?alt=media" alt="Add field menu showing new field, computed field, lookup, rollup, and AI autofill options"><figcaption><p>Extend the Tickets table using the Add field menu.</p></figcaption></figure>

The same menu includes computed fields, lookups, rollups, and AI autofill. See [Computed fields](../computed-fields/) and [Relationships](../relationships/).

For connected data, update the source schema where required, then [sync schema changes](../../synced-tables/syncing-schema-and-data.md). Changing a component's display format does not change the source column type.

## Configure columns in Classic App Builder

Select the table component and configure the column's display type. For example, use an image display for a field containing image URLs. Check a record with a value and a record with an empty value.

![Change a column display type in Classic App Builder](https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkLMYHr5-4poYmffLsc%2F-MkLNKbzmq7FV0I_tQzb%2Ftestgif83.gif?alt=media\&token=93c6eccc-4b74-47b9-8359-2cb992d3ac9e)

![Reorder component columns](https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkLMYHr5-4poYmffLsc%2F-MkLMtFm531pGQDAFb1J%2Ftestgif82.gif?alt=media\&token=88e3e5e3-d2ca-4d2c-847f-fc5bd333616d)

![Choose which columns appear in a component](https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjehuplWWd6OK_2hI_D%2F-Mjel8tSRCRhfMhmMk2u%2Ftestgif43.gif?alt=media\&token=174adf47-d7d9-49f9-a83e-72c4ce31ff9d)

Reorder columns to match your task, and hide fields that do not need to appear in the component. Hidden fields remain in the data source; use permissions to control access.

For Data Editor view controls, follow [Navigate the Data Editor](../new-ui-and-ux.md).
