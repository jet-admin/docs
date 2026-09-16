---
icon: bridge
---

# Self-hosted Jet Bridge

Jet Bridge is an open-source backend that connects the Jet Admin interface to supported resources through an API. In this deployment model, you operate the bridge service and its connection to your resources.

## Choose an installation method

* [Python installation](../../../user-guide/data-sources/databases/sql-databases/python-app-installation.md)
* [Docker installation](../../../user-guide/data-sources/databases/sql-databases/docker-installation.md)
* [Django integration](../../../user-guide/data-sources/databases/django-framework-package.md)

Follow the requirements and configuration for the chosen method.

## Understand the components

| Component           | Responsibility to confirm                                                              |
| ------------------- | -------------------------------------------------------------------------------------- |
| Jet Admin interface | App interface and its service dependencies.                                            |
| Jet Bridge          | API service, runtime configuration, authentication integration, and resource requests. |
| Database or API     | Source data, credential scope, and its own recovery process.                           |
| Network and proxy   | Reachability, HTTPS configuration, and any required forwarding.                        |

The bridge is not the same as deploying all Jet Admin services On-Premise. Review the actual request path and authentication dependencies of your installation instead of assuming it has no external service communication.

## Configure and verify

1. Install the bridge using the selected guide.
2. Review [Configuration](configuration.md) and the relevant resource settings.
3. Confirm the expected browser, bridge, resource, and authentication connectivity.
4. Test a permitted read and write with synthetic data.
5. Test a denied action with a restricted account.
6. Document how the bridge is monitored, updated, and recovered.

For special setups, see [SSO on self-deployed Jet Bridge](sso-on-self-deployed-jet-bridge.md) and [Using a self-deployed HTTP proxy](using-self-deployed-http-proxy.md). For failures, use [Jet Bridge common problems](common-problems.md).
