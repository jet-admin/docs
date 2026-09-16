# Import and export data

Bring an existing file into Jet Tables and verify the imported records before using them in an app.

## Before you start

Prepare a **CSV, XLS, XLSX, or JSON** file. For tabular files, use clear column names and consistent values within each column. Keep a copy of the original file so you can compare the result.

## Import a file

1. Open the Jet Tables setup window.
2. Select **Import from File**.
3. Select **Choose File**, or drag your file into the upload area.
4. Review **Advanced settings** if you need to adjust encoding or automation settings.
5. Select **Import file**.

<figure><img src="https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2F95aH852TE8EMM9Pa7Vy9%2F03-import-file.png?alt=media" alt="File import dialog with Choose File, supported formats, Advanced settings, and Import file"><figcaption><p>Upload an existing file to bring your data into Jet Tables.</p></figcaption></figure>

## Verify the import

Compare the imported record count with the input. Inspect a few records, including dates, numbers, blank values, and text containing special characters. Check that the field types match how you intend to use the values.

If text is garbled, review encoding. If numbers or dates are interpreted incorrectly, check the source format and field configuration before relying on the import.

## Export data

Open the collection you want to export and use its export option. Check which records the export includes, especially when filters are active, and select an available format.

Open the exported file and compare its columns and record count with the intended selection. A data export is not an export of your entire app configuration.

Continue with [Field types](../data/fields/field-types.md).
