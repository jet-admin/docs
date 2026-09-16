# Gmail connection blocked by Google

If Google displays “This app is blocked” while connecting Gmail, capture the exact message and identify the account you are trying to connect.

## Start with the built-in Gmail connection

1. In Jet Admin, open **Data → Add Resource**.
2. Select **Gmail**.
3. Sign in to the Google account whose mailbox you want to connect.
4. Review the requested access and complete the connection if Google permits it.

This is the built-in connection flow. If you are following instructions for a custom OAuth client and are being asked for a redirect URI, first check whether the [Gmail integration](https://docs.jetadmin.io/user-guide/data-sources/business-apps/gmail) meets your task.

## Google blocks authorization

A blocked authorization is different from an incorrect Jet Admin password. If this is a managed Google Workspace account, ask its administrator to check whether an organizational policy is involved.

If the block persists, contact Jet Admin support with:

* The app URL and exact Google error.
* Whether this is a personal or managed Workspace account.
* Whether the Gmail mailbox is different from the account used to sign in to Jet Admin.
* The time of the attempt and a screenshot with sensitive details removed.

The error alone does not establish whether the cause is an organization policy or an integration issue. Do not bypass the block or create a replacement OAuth configuration without confirming the cause.

## Verify the connection

Once authorization succeeds, confirm the intended Gmail resource appears and test a read operation before using it in an automation.

_Last reviewed: September 16, 2026._
