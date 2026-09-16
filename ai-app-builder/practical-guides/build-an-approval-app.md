# Build an approval app

Build a purchase-request app with a manager decision queue.

## Prepare data

Use PurchaseRequests with a unique ID, Requester, Amount, Reason, Status, Decision reason, Decided by, and Decided at. Map these proposed fields to your actual schema. Prepare a staff user and a manager user.

## Build the first version

1. Select the source.
2. Adapt this prompt:

> Build a purchase-request app using PurchaseRequests. Staff can submit a request with Amount and Reason and see the requests they are allowed to access. Managers have a queue of Pending requests. Start with the lists and detail views before adding decision actions.

3. Check the records visible to each role.

## Add the decision flow

> Add Approve and Reject actions for managers on a Pending request. Require a reason for rejection. Record the decision, decision maker, and timestamp. Prevent a completed request from being decided again.

Configure the action permissions and inspect the generated update logic. Use the [approval workflow guide](../../workflow/practical-guides/create-an-approval-process.md) when the decision belongs in a workflow.

## Test both outcomes

* Approve one Pending test request and verify its stored status and decision fields.
* Reject a different request and verify its reason.
* Try to decide a completed request again.
* Try the manager action as a staff user and confirm it is denied.

Add notifications only after the decision flow works, and test them with designated recipients.

Next: [Test and publish](../test-and-publish/).
