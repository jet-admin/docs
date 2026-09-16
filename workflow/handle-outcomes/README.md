# Handle outcomes

Decide what should happen when an operation succeeds, fails, or arrives more than once.

* [Run actions after component success or failure](component-success-and-failure-actions.md) covers callbacks in a component's Actions configuration.
* [Handle failures and prevent duplicate processing](handle-failures-and-prevent-duplicate-processing.md) covers failure diagnosis and repeat-safe process design.
* [Create an approval process](../practical-guides/create-an-approval-process.md) adds a human decision before a configured action.

Component callbacks are not a substitute for a workflow's internal dependencies. Test both the visible response and the stored data.
