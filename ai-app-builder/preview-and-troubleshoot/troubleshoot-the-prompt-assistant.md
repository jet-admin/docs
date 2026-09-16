# Troubleshoot the AI Assistant

Identify whether the problem is the request, generation, Preview, data, or access before making another broad change.

| Symptom                             | What to check                                        | Next step                                                                                                           |
| ----------------------------------- | ---------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| The assistant uses the wrong source | Selected resource and exact table names              | [Select the intended source](../ai-assistant/select-data-sources.md) and clarify the request.                       |
| A field is missing                  | Source schema and connection access                  | [Inspect the connection](../create-an-app/connect-existing-data.md) before changing the UI.                         |
| The wrong page or component changes | Target and scope in the prompt                       | [Request one focused correction](../refine-an-app/request-focused-changes.md).                                      |
| A file will not attach              | File picker restrictions and upload error            | [Check the attachment workflow](../ai-assistant/upload-images-and-files.md).                                        |
| Dictation is unavailable            | Browser permission and microphone input              | [Check dictation setup](../ai-assistant/type-or-dictate-a-prompt.md) or type the request.                           |
| Preview is blank or disconnected    | Session status and recent logs                       | [Inspect Console](inspect-app-console-and-logs.md); use [Restart Preview](control-app-preview.md) when appropriate. |
| An action fails                     | Inputs, source permissions, and actual source result | [Test once with a safe record](../test-and-publish/check-data-actions-and-user-access.md).                          |
| A user sees unexpected records      | Authentication, user properties, and record rules    | [Compare user experiences](preview-as-an-invited-user.md) and check enforcement.                                    |
| Usage is limited                    | Account allowance and usage messages                 | Check [How credits work](../../account/credits-and-rate-limits/how-credits-work.md).                                |

## Ask for help with a reproducible case

Include the app page, time, relevant prompt, selected resource and model, expected result, actual result, and a sanitized error. State whether the problem also occurs in the published app.

Before repeating a create, update, or send action, confirm whether the first attempt already completed. Keep a failing test case so you can verify the eventual fix.
