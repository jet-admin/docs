---
icon: globe
---

# Custom domains

Give the published app an address on a domain you control.

## Before you start

Have access to your DNS configuration, identify the app and environment, and choose the subdomain you want to use. Verify that the published app works at its existing address first.

* [Connect a custom domain](configuring-a-custom-domain.md) for the current app setup flow.
* [Troubleshoot a custom domain](troubleshoot-a-domain.md) for DNS, connection, or login failures.
* [On-Premise custom domain configuration](../cloud-jet-bridge-and-on-premises/on-premise/.env-configuration-local-host/custom-domain-configuration-on-premise.md) for self-hosted deployments.

## Verify the whole user journey

A configured domain is only one part of the release. Test loading, sign-in, a permitted data action, and a restricted action at the new address.

Use the values supplied by the current setup flow for your app. Do not reuse a DNS target or callback URL from a different deployment.
