# Review AI-generated changes

Treat AI-generated pages, queries, and workflows as changes that need an access review before release.

## Review the request

State the audience, permitted data, and prohibited actions in the request. For example:

> Add a ticket page for support agents. Agents may view and update tickets for their assigned customer. They must not delete tickets, change customer ownership, or access another customer's records.

This describes an intended policy. It does not prove that the generated implementation enforces it.

## Review the result

Inspect the pages, actions, queries, resource connections, and workflows affected by the change. Check:

* Which identity each data request uses.
* How the relevant customer or user identifier is obtained.
* Whether reads and writes enforce the same scope.
* Whether hidden UI controls have corresponding authorization.
* Whether errors or logs expose credentials or unnecessary data.

Use synthetic examples in prompts and attachments. Only include data the selected AI service is intended to process under your organization's policy.

## Validate and release

Compare the implementation with the intended policy using [allowed and denied tests](test-access.md). Include a user from another customer and a user with missing access properties.

Preview the app as the intended user, then test the published version with a separate test account through your release process. Record the version and results so later changes can be checked against the same expectations.
