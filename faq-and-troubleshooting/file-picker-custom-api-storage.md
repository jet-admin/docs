# Custom API storage is missing from File Picker

In Classic App Builder, File Picker selects a storage configuration. If you have added a REST API resource but cannot select it for uploads, check whether a storage and its upload query have been configured.

## Check the storage setup

1. Open the resource's **Storages** section in the Data Editor.
2. Use **Create Storage** if the required storage has not been configured.
3. Configure the required **Upload** query for your storage.
4. Return to File Picker and choose **Save to Storage** as its output format.
5. Select the configured storage and test with a small, non-sensitive file.

See [Data Source Storage](https://docs.jetadmin.io/user-guide/data/file-storage-and-uploading/data-source-storage) for the setup flow and [File](https://docs.jetadmin.io/classic-app-builder/design-and-structure/components/fields/file) for File Picker settings.

## I cannot bind the upload parameters

Check the upload endpoint's required body fields and encoding. The upload-query editor may not expose the same controls as the general REST API builder.

If a required input or binding control is unavailable, send support the app URL, storage type, required parameter names, and a sanitized screenshot of the upload-query editor. Explain which file or metadata value you need to pass. Do not include API keys or authorization headers.

## Verify the upload

Check that the file reaches the intended storage and that the app record references the intended file. Confirm access using an end-user account before making the upload flow available to customers.

_Last reviewed: September 16, 2026._
