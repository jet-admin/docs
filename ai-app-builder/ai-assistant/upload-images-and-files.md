# Upload images and files

Attach an image or file to give the assistant reference material for a request. A screenshot can explain a layout; a document can describe the required behavior.

## Attach files before creating an app

{% hint style="info" %}
Attachments in the initial app-creation prompt are a development preview.
{% endhint %}

1. Open the app-creation prompt and describe the app you want.
2. Use the attachment control to choose files, such as a CSV, a document, or an image.
3. Wait for the attachments to appear in the prompt box. Remove any files you do not want to include.
4. Explain how the assistant should use each file, review its proposed plan, then confirm generation.

![Files attached to the initial app-creation prompt](https://250870895-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F8xy7P3kSppSd57K7pcpL%2Fuploads%2F9pWaYPY4RbE6nEZF6oCj%2Fprompt-attachments.webp?alt=media)

> Build a support dashboard using the attached CSV as starting data in Jet Tables. Use the attached image as a layout reference.

If you want to create records from a file, explicitly ask for an import. See Import and export data for the assistant import workflow and how to check the result.

## Attach reference material in an existing app

1. Open the chat for your task.
2. Click the **paperclip** beside the message input.
3. Choose your image or file and wait for the attachment to appear.
4. Explain what the assistant should take from it: layout, wording, requirements, or another specific detail.
5. Send the request with the attachment.

{% embed url="https://app.arcade.software/share/ybW6HlbAIHm3JwWUna3X" %}

> Use the attached screenshot as a layout reference for the Tickets page. Keep the connected Tickets data and existing permissions. Put the search field above the list and show Priority beside Status.

## Use a file from an earlier message

You can refer to a file already attached in the same conversation. Name the file and explain what to do with it, especially when the conversation contains several attachments.

> Import tickets.csv from my earlier message into the Tickets collection using the bulk import tool. Show the field mapping and import results.

The assistant can use the uploaded file's URL from earlier messages. For CSV data, ask for a bulk import rather than creating each record separately. Check previous import results before repeating a request so you do not add the same rows twice.

## Check the result

Compare the requested details with Preview. If the assistant misses something, refer to that part of the attachment in a focused follow-up.

An attachment provides context. To use a database or business application as live app data, select a connected data source. To import rows into a table, follow Import and export data.

## If an upload fails

Check the file picker and any upload error for supported types and size restrictions. Retry one file at a time after checking that the file opens locally. Do not assume that a model's context-window number is an attachment size limit.

Next: Request focused changes.
