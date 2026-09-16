# Diagnose resource and deployment errors

Trace the failed operation from the published app to the resource or service responsible for it.

## Isolate the failure

1. Record the environment, user role, page, action, and time.
2. Determine whether the app itself loads.
3. If loading works, identify the query, resource, API, or workflow used by the failing action.
4. Check the configured connection, credential scope, and required network path.
5. Reproduce with a safe read or synthetic test record.
6. Inspect the relevant logs before changing configuration.

A successful connection test is not proof that every query or write is authorized. Check the specific failed operation and identity.

## Use the deployment-specific checks

| Deployment             | Diagnostic path                                                                                                                                                                                                  |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Cloud                  | App [System logs](../../access-and-sharing/audit-logs-privacy-and-security/investigate-system-logs.md), resource settings, and relevant provider diagnostics.                                                    |
| Self-hosted Jet Bridge | Bridge service logs, [Common Problems](../cloud-jet-bridge-and-on-premises/jet-admin/common-problems.md), and [Configuration](../cloud-jet-bridge-and-on-premises/jet-admin/configuration.md).                   |
| On-Premise             | [Service Health Check](../cloud-jet-bridge-and-on-premises/on-premise/service-health-check.md), affected service logs, and [Common Problems](../cloud-jet-bridge-and-on-premises/on-premise/common-problems.md). |

Use the actual service URLs from your environment when following health checks. A service responding successfully does not establish that authentication, resource access, or the full user flow works.

Share redacted errors and reproduction steps with the responsible operator. After correction, repeat the failed operation and [the affected release checks](../publish-your-app/verify-a-release.md).
