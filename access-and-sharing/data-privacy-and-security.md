---
icon: database
---

# Security and data handling

Review data handling for the features and deployment you actually use. Storage, request processing, diagnostic logs, and AI inputs are separate parts of that review.

## Identify where data is handled

| Area                         | What to establish                                                        |
| ---------------------------- | ------------------------------------------------------------------------ |
| Connected databases and APIs | Where the source records live and how Jet Admin requests are authorized. |
| Jet Tables                   | The hosted data stored in the Jet Tables resource.                       |
| Jet Bridge                   | Where the bridge runs and which database or API requests it handles.     |
| On-premise deployment        | Which components you operate and their network dependencies.             |
| AI features                  | Which prompts, files, and data are supplied to the selected service.     |
| Logs and exports             | What they contain, who can access them, and how long they are retained.  |

Do not assume that using an external database means no data is processed elsewhere. Review the configured request path and the applicable service documentation or agreement.

See [the architecture guide](../jet-bridge-deployment/cloud-jet-bridge-and-on-premises/cloud.md), [Jet Bridge hosting](../jet-bridge-deployment/cloud-jet-bridge-and-on-premises/jet-admin/), and [on-premise deployment](../jet-bridge-deployment/cloud-jet-bridge-and-on-premises/on-premise/) for deployment-specific guidance.

## Credentials and network access

Use appropriately scoped credentials for each resource and keep secrets out of app code, prompts, screenshots, and shared logs. Review credential ownership and rotation with the team operating the data source.

Network restrictions such as a VPN or private network can reduce exposure. They do not replace authentication, authorization, maintenance, or monitoring.

## Recovery responsibilities

Distinguish restoring an app configuration from restoring records in a connected database. Before relying on recovery, confirm what is backed up, how restoration works, retention, and who owns the process for each system.

Test recovery in an appropriate environment. Do not assume an interface restore reverses data writes made by users, APIs, or workflows.

For access verification, use [the access test checklist](overview/test-access.md); for operational investigation, see [Audit trail and system logs](audit-logs-privacy-and-security/).
