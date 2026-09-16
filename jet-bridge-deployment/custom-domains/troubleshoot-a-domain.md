# Troubleshoot a custom domain

First determine whether the problem affects the domain alone or the app at every address.

## Check the symptom

| Symptom                                               | Next check                                                                             |
| ----------------------------------------------------- | -------------------------------------------------------------------------------------- |
| Existing app address works, custom domain does not    | Exact hostname, configured DNS records, and domain status in Jet Admin.                |
| The wrong site opens                                  | DNS destination and which app the domain is configured for.                            |
| The browser reports a connection or certificate error | Hostname and HTTPS configuration; inspect the error before proceeding.                 |
| App loads but sign-in fails                           | Identity-provider callback/redirect values and the app's authentication configuration. |
| App loads but data fails                              | Resource connectivity and permission checks, not just DNS.                             |

## Investigate in order

1. Record the exact address, error, and time.
2. Confirm the app and environment in **More → General → Custom Domain**.
3. Compare the DNS record type, name, and target with the current setup instructions.
4. Check for conflicting records or a hostname entered in the wrong DNS field.
5. Compare behavior at the existing address and the custom address.
6. Retest the published app after correcting the identified issue.

Do not bypass a browser security warning to declare the domain working. For On-Premise, include [domain configuration](../cloud-jet-bridge-and-on-premises/on-premise/.env-configuration-local-host/custom-domain-configuration-on-premise.md) and [Nginx configuration](../cloud-jet-bridge-and-on-premises/on-premise/.env-configuration-local-host/nginx-configuration.md) in the investigation.

For successful loading followed by login failure, use [Published app access fails](../logs-and-troubleshooting/published-app-access-fails.md).
