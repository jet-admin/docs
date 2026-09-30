# Control app Preview

Use the toolbar above Preview to check screen sizes, expand the app, and control its preview session.

## Desktop, Tablet, and Mobile

1. Open the device menu near **Console**.
2. Choose **Desktop**, **Tablet**, or **Mobile**.
3. Inspect the same page at each size.
4. Check navigation, tables, forms, dialogs, and long labels.

![Preview device menu with Desktop, Tablet, and Mobile choices](https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2Fn0k4rCD9Xa40SIEv02kP%2F07-device-menu.png?alt=media)

![Tickets page displayed in the Mobile preview frame](https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2F2Mu3VmUiUWGN3Hv7WGEL%2F08-mobile.png?alt=media)

![Tickets page displayed in the Tablet preview frame](https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2FISDMC4VqQh5dgP0jp5KD%2F09-tablet.png?alt=media)

A device preview helps find layout problems. Also test important interactions on the actual devices and browsers your users use.

## Full screen

Click the full-screen icon beside the device control to expand Preview. Use the full-screen control again to return to the builder layout. Full screen expands your working view; it does not publish the app.

## Stop and restart

1. Save or finish any in-progress form work.
2. Open the **…** menu at the right of the Preview toolbar.
3. Choose **Stop Preview** to stop the preview session, or **Restart Preview** to start it again.
4. After a restart, wait for the app to load and reopen the page you were checking.

![Preview menu showing Stop Preview and Restart Preview](https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2F2Up8uXLAhDw0TF5YXeY9%2F10-preview-controls.png?alt=media)

Treat unsaved form input and temporary UI state as disposable during a restart. Restarting Preview is not a way to undo changes already saved to a connected data source.

## Free a preview slot

If the builder says you cannot run more previews, open an app preview you are no longer using, including one in another browser tab. Open its **…** menu and select **Stop Preview**, then return to the app you want to work on.

Stopping an unused preview frees a simultaneous preview slot. The Stop Preview control is part of the development-preview updates, so its availability may differ by builder version.

## Preview during app creation

For a newly generated app, wait for the assistant to finish initial generation before expecting Preview to appear. A blank preview area during this step does not by itself mean the app has failed.

When starting from a template, allow template setup to finish before testing the app. Preview startup is optimized, but the time needed depends on the app and its dependencies.

## Preview after importing an app

When importing an app archive, allow the import to finish before expecting Preview to start. The builder now waits for import completion before starting the preview.

## If Preview does not recover

Capture the error and check Console and logs. Record the route and the last action. Avoid repeating a write action until you know whether it completed.

Next: Preview as an invited user.
