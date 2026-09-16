# Password-reset or invitation email not received

If a user cannot receive a password-reset or invitation email, first check the app, email address, and sign-in method involved.

## Check the sign-in method

Use the app's sign-in page. If the user normally signs in through Google or another identity provider, use that provider's recovery process for its password. An app password reset and an identity-provider password reset are different operations.

## Check email delivery

1. Confirm the exact email address, including spelling, with the user.
2. Request recovery from the affected app's sign-in page.
3. Ask the user to check spam, junk, and any organizational quarantine.
4. If your organization filters email, ask the mail administrator to inspect delivery logs around the request time.
5. If the app uses customized transactional email, have the app administrator check its configured sending domain and email settings.

For setup, see [Custom Domain and Transactional Emails](https://docs.jetadmin.io/classic-app-builder/design-and-structure/core-concept/jet-ui/layouts-and-branding/custom-domain-and-transactional-emails).

## The user was deleted, but an invitation says the account exists

Check both the app's users and pending invitations. If neither shows the account but the conflict remains, ask support to investigate its state. Avoid repeatedly deleting or recreating accounts to work around the error.

## Still unable to sign in?

Send support the app URL, affected email address, sign-in method, exact error, and the time and timezone of the latest attempt. Mention any checks by the mail administrator.

Never send passwords, reset links, or one-time codes. After support provides a recovery step, have the affected user confirm that they can sign in to the intended app.

_Last reviewed: September 16, 2026._
