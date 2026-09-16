---
icon: server
---

# On-Premise deployment

Deploy Jet Admin services on infrastructure your organization operates.

## Setup sequence

1. Review [Prerequisites](prerequisites.md) for supported software, capacity, and network requirements.
2. Follow [Deploy On-Premise Jet Admin with Docker](deploy-on-premise-jet-admin-with-docker.md) or the applicable [deployment guide](deploy-jetadmin-on-premise.md).
3. Configure the environment using [.env configuration](.env-configuration-local-host/).
4. Complete required domain, authentication, and integration setup.
5. Run [Service Health Check](service-health-check.md).
6. Test the complete [published-app journey](../../publish-your-app/verify-a-release.md) with representative users.

Use the installation path appropriate to your deployment. Follow its supported versions and configuration rather than mixing examples from separate guides.

## Configure the services you use

* [Custom domain configuration](.env-configuration-local-host/custom-domain-configuration-on-premise.md)
* [Nginx configuration](.env-configuration-local-host/nginx-configuration.md)
* [Email sending configuration](.env-configuration-local-host/email-sending-configuration.md)
* [Enabling AI features](.env-configuration-local-host/enabling-ai-features-in-on-premises.md)

Hosting the application yourself does not make every feature independent of external services. Identify the network dependencies of authentication, email, AI, and connected resources before restricting traffic.

## Operate and recover

Assign owners for monitoring, updates, secrets, and backups. Use the [Update guide](update.md) for platform maintenance and confirm configuration and database recovery separately.

For errors, start with [On-Premise common problems](common-problems.md) and the affected service's logs. Use [Cross-Instance Backup & Restore](../../environments-releases-and-version-control/version-control/cross-instance-backup-and-restore.md) when moving supported backups between instances.
