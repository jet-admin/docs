# Edit components in Preview

Select an element in your app preview to adjust its appearance or ask the assistant for a focused change.

{% hint style="info" %}
The element style editor is a development preview. Available controls may differ in your builder version.
{% endhint %}

## Select an element

1. Open the correct page in **Preview** and wait for it to load.
2. Click **Edit** in the Preview toolbar.
3. Select the element you want to change.
4. Check the highlighted area before editing. A selection may cover a containing region rather than a single label.

## Adjust styles visually

Use the element editor to adjust backgrounds, including gradients, borders, corner radius, shadows, opacity, and spacing. Text elements also show typography controls. Expand a style section to see its settings.

![Element editor with styling controls beside the selected dashboard element](https://250870895-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F8xy7P3kSppSd57K7pcpL%2Fuploads%2FGRilrSD5NPa8UhLK2G6T%2Felement-editor.webp?alt=media)

Your adjustments appear in Preview before you save them. The pending-changes indicator shows how many edits have not been saved.

* Select **Discard** to cancel the pending visual edits.
* Select **Save Changes** to ask the assistant to apply the styles to the app's source code.

Wait for the assistant to finish, then check the result. Saving uses the assistant to update the source so the changes persist after reloading.

## Edit text

Static text can be edited directly where the editor exposes a text control. Text generated from variables or other app logic may not be editable directly. Ask the assistant to update that content instead.

> Change the Tickets heading to Support tickets on this page. Keep the ticket table, data source, and actions unchanged.

For repeated components or shared text, specify whether the change should affect only the selected element or every instance. Do not assume a visual edit automatically applies to matching elements elsewhere.

## Describe a change to the assistant

Enter a focused instruction in the selected element's chat input. The selection gives the assistant context for the request. In builder versions that show **What to change?**, enter the instruction there and select **Submit**.

For behavior that spans several components, use [a focused chat request](request-focused-changes.md) and name the affected pages.

## Check the result

Leave Edit mode and verify the change in the app. Check nearby controls still work. For a form or action, test with a safe record.

If the wrong region is selected, close the selection and select again. Use [Themes and appearance](../themes-and-appearance/) for app-wide theme settings.
