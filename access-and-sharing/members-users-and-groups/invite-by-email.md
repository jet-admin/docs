# Invite users by email

Invite a specific person and select the team they should join.

**Before you start:** use an account allowed to manage membership, choose the intended team, and check that the published app is ready for the recipient.

## Send an invitation

1. Open **Users → Users**.
2. Select **Invite Member**.
3. In **Invite with Email**, enter the recipient's email.
4. Open the team selector and choose the appropriate team. Review [Administrator, Editor, and Read Only](../teams-and-roles/built-in-roles.md) before choosing.
5. Check the email and team, then select **Send Invite**.

![Invite members dialog with separate email and link invitation controls](../../.gitbook/assets/02-invitations.png)

The screenshot shows Administrator selected. This is an example of the current selection, not a recommendation for every invitation.

## Verify the result

Ask your test recipient to complete the invitation flow. Confirm that the resulting user appears in the Users list with the intended team and can open the published app.

The dialog's unpublished-changes warning means non-builder users will see the published version. Publish the intended app version through your normal release process before comparing their experience with a new builder change.

## Troubleshooting

If an invitation is missing, check the email spelling and the recipient's spam or quarantine folders. Confirm that they are opening the intended app with the invited account before changing permissions.

If sign-in works but access is incorrect, use [Test access before publishing](../overview/test-access.md).
