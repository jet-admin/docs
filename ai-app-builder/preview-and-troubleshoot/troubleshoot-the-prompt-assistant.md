# Troubleshoot the AI Assistant

Identify whether the problem is the request, generation, Preview, data, or access before making another broad change.

| Symptom                             | What to check                                        | Next step                                              |
| ----------------------------------- | ---------------------------------------------------- | ------------------------------------------------------ |
| The assistant uses the wrong source | Selected resource and exact table names              | Select the intended source and clarify the request.    |
| A field is missing                  | Source schema and connection access                  | Inspect the connection before changing the UI.         |
| The wrong page or component changes | Target and scope in the prompt                       | Request one focused correction.                        |
| A file will not attach              | File picker restrictions and upload error            | Check the attachment workflow.                         |
| Dictation is unavailable            | Browser permission and microphone input              | Check dictation setup or type the request.             |
| Preview is blank or disconnected    | Session status and recent logs                       | Inspect Console; use Restart Preview when appropriate. |
| An action fails                     | Inputs, source permissions, and actual source result | Test once with a safe record.                          |
| A user sees unexpected records      | Authentication, user properties, and record rules    | Compare user experiences and check enforcement.        |
| Usage is limited                    | Account allowance and usage messages                 | Check How credits work.                                |

## Preview limit reached

Open an unused app preview, select **… → Stop Preview**, and return to the app you want to work on. See Control app Preview.

## The assistant appears idle during a tool call

Long-running actions can show progress while the assistant uses tools. Check the active action and any available details before sending the same request again. If progress stops or an error appears, record the action, time, and error for support.

## Preview is blank during generation

Wait for initial app generation to finish. The builder holds Preview until that step completes. If generation is complete and Preview remains blank, check Console and logs.

## Recurring request timeouts

A fix for recurring request timeouts has been deployed and is being monitored. If the error continues, record the time, prompt, and visible error for support. Before retrying a request that writes data, check whether any records were already created or changed.

## Ask for help with a reproducible case

Include the app page, time, relevant prompt, selected resource and model, expected result, actual result, and a sanitized error. State whether the problem also occurs in the published app.

Before repeating a create, update, or send action, confirm whether the first attempt already completed. Keep a failing test case so you can verify the eventual fix.
