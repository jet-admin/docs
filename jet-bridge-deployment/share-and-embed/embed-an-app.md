# Embed an app

Display an app inside another website or tool when your app's sharing mode and the host support embedding.

## Choose the appropriate workflow

The existing Classic builder provides documented workflows for [a generated sharing link](../../classic-app-builder/preview-and-publish/embed-apps/embedding-app-using-a-generated-link.md) and [iFrame/HTML embed code](../../classic-app-builder/preview-and-publish/embed-apps/embedding-app-using-iframe-html.md). Those tutorials use **Share → Public Share → Public Access Link**.

The current AI builder's inspected Share dialog contains membership invitations. Do not assume its invitation link is equivalent to Classic public sharing or generated embed code.

## Embed and verify

1. Publish and verify the app outside the host site first.
2. Confirm the supported sharing or embedding method for your app.
3. Obtain the appropriate app URL or generated embed code.
4. Add it through the host site's supported embed or HTML component.
5. Open the host page as an intended user.
6. Check sign-in, navigation, sizing, permitted actions, and restricted data access.

For a Classic embed, select the intended team before distributing public sharing access. Review the resulting access rather than assuming the host site's own login protects the embedded app.

## Troubleshoot an embedded app

If the app works directly but fails inside the host, capture the browser error and compare the sign-in and framing behavior. Check the host's embed support and the app's authentication requirements. Do not disable access controls just to remove an embedding error.

If a supported embedded flow is unavailable, provide a normal link to the published app. Continue with [published-app access troubleshooting](../logs-and-troubleshooting/published-app-access-fails.md) for sign-in or permission failures.
