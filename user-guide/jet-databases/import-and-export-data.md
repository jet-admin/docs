# Import and export data

Bring an existing file into Jet Tables and verify the imported records before using them in an app.

## Before you start

Prepare a **CSV, XLS, XLSX, or JSON** file. For tabular files, use clear column names and consistent values within each column. Keep a copy of the original file so you can compare the result.

## Import a CSV with the assistant

{% hint style="info" %}
The assistant's collection import tool is a development preview. Manual import remains available.
{% endhint %}

1. Attach the CSV to your prompt, either when creating an app or in an existing app's chat.
2. Name the target Jet Tables collection. Say whether the assistant should use an existing collection or create one.
3. Ask the assistant to use bulk file import and specify how you want existing records handled. If the CSV was attached in an earlier message in the same conversation, refer to it by filename.
4. Review the import action details, including the field mapping and the counts of created and failed records.
5. Check the records in the Data workspace before using them in your app.

> Import the attached tickets.csv into the existing Tickets collection. Map Ticket title to Name and Owner to Assigned to. Add the new rows and keep existing records.

The assistant can inspect the file's columns and map them to collection fields even when their names differ. The import tool processes the file in bulk, avoiding a separate assistant create-record call for every row.

![File-import action showing field mapping and import results](https://250870895-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F8xy7P3kSppSd57K7pcpL%2Fuploads%2FFBA1Ao7I0EUPss7Tizhh%2Fcollection-import.webp?alt=media)

If the result reports errors, review which rows succeeded before retrying. Ask the assistant to explain the errors and correct the mapping or source values as needed.

## Import a file manually

1. Open the Jet Tables setup window.
2. Select **Import from File**.
3. Select **Choose File**, or drag your file into the upload area.
4. Review **Advanced settings** if you need to adjust encoding or automation settings.
5. Select **Import file**.

<figure><img src="https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2FpfDjNrk1cQ4h18MWVtin%2FS06-import-dialog.jpg?alt=media" alt="Import from File dialog with Choose File and Import file"><figcaption><p>Choose a supported file, review its settings, and import it.</p></figcaption></figure>

## Verify the import

Compare the imported record count with the input. Inspect a few records, including dates, numbers, blank values, and text containing special characters. Check that the field types match how you intend to use the values.

If text is garbled, review encoding. If numbers or dates are interpreted incorrectly, check the source format and field configuration before relying on the import.

## Export data

Open the collection you want to export and use its export option. Check which records the export includes, especially when filters are active, and select an available format.

<figure><img src="https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2FPUqeuCr8Qms4D3Oqe8r2%2FS08-export-formats.jpg?alt=media" alt="Records Export formats: CSV, Excel, JSON, HTML, and TXT"><figcaption><p>Choose an export format and check which records are included.</p></figcaption></figure>

Open the exported file and compare its columns and record count with the intended selection. A data export is not an export of your entire app configuration.

Continue with Field types.
