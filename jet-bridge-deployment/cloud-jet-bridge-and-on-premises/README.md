---
icon: server
---

# Deployment options

Choose where the app's supporting services run and who will operate them.

| Approach               | What you operate                                                                                     | Start with                           |
| ---------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------ |
| Cloud                  | Your app configuration, connected resources, identities, and access policy                           | [Cloud](cloud.md)                    |
| Self-hosted Jet Bridge | The bridge service and its resource connectivity; the Jet Admin interface remains a separate service | [Self-hosted Jet Bridge](jet-admin/) |
| On-Premise             | The deployed Jet Admin services and their supporting infrastructure                                  | [On-Premise deployment](on-premise/) |

## Decide before installation

Document where source data lives, which services may communicate, who manages credentials, and which authentication system users need. Include AI providers, email, and external integrations in the dependency review when you use them.

Confirm plan and deployment availability for your organization before committing to a hosting approach. The comparison above describes operating responsibilities, not a guarantee of a particular network or data-processing boundary.

## Follow the matching setup path

Use the installation and configuration guides under the selected approach. Confirm required software and versions from the guide for that deployment; do not combine commands from different installation methods.

After setup, validate service health, resource access, user sign-in, and [the published app](../publish-your-app/verify-a-release.md). A healthy service response alone does not prove the whole application works.

See [resource and deployment troubleshooting](../logs-and-troubleshooting/resource-and-deployment-errors.md) for failures and [Security and data handling](../../access-and-sharing/data-privacy-and-security.md) for storage and recovery responsibilities.
