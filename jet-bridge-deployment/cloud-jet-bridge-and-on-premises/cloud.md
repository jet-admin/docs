# ⛅ Cloud

Use Jet Admin's hosted services while managing your app configuration, users, and connected resources.

## Prepare the app

1. Identify the database or API used by each environment.
2. Configure the required connections and appropriately scoped credentials.
3. Set up user membership, authentication, and permissions.
4. Test representative reads, writes, and denied actions.
5. [Publish](../publish-your-app/) and [verify](../publish-your-app/verify-a-release.md) the intended app version.

## Review data handling

Distinguish source data storage from request processing, logs, exports, uploaded files, and AI inputs. Connecting an external database does not by itself establish that no data is processed by other services.

Review the configured resource and feature behavior for your app. See [Security and data handling](../../access-and-sharing/data-privacy-and-security.md) for the questions to resolve, including Jet Tables and recovery scope.

## Operational checks

Confirm that the intended users can reach the app and that the required resources are reachable through the configured connection path. Assign an owner for credential rotation, membership review, and resource recovery.

For connection failures, use [Diagnose resource and deployment errors](../logs-and-troubleshooting/resource-and-deployment-errors.md). If you need to operate a bridge or the application services yourself, compare [deployment options](./).
