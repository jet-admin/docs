# Data is not loading

If an app, table, or query stops loading, identify which part fails before changing the database or rebuilding the page.

## Locate the failure

1. Record the affected app URL, environment, error message, and the time the problem began.
2. Check whether it affects the whole app, one page, or a particular component.
3. If the builder opens, test the underlying data-source query separately from the component.
4. Note recent changes to the schema, query, credentials, permissions, or network.
5. If several previously working pages fail without changes, contact support with those examples.

## Choose the matching symptom

| Symptom                                              | What to check next                                                                                                  |
| ---------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| “App failed to load,” blank builder, or HTTP 502/503 | Record the failing page/request and whether other users are affected. These symptoms alone do not identify a cause. |
| Supabase “maximum clients” or connection-limit error | Ask the database administrator to inspect active connections, pool usage, and provider limits.                      |
| Query timeout                                        | Check whether the same query succeeds at the data source and whether the failure is consistent.                     |
| Columns or tables missing after a schema change      | Review the schema-sync guide linked below before changing the resource.                                             |
| “Nothing found” only when filters are applied        | Check filter values, bound inputs, and the permissions of the test user.                                            |
| “'TextClause' object has no attribute 'filter'”      | Capture the query and filter setup and contact support; do not assume this is a normal empty-result case.           |
| 403 or access denied                                 | Follow the user-permission troubleshooting guide.                                                                   |

## Supabase connection limits

A connection-limit error concerns database connections, not necessarily the number of people viewing a page. Multiple components or queries can contribute to connection usage.

Ask your database administrator to inspect pool usage and confirm the connection mode and endpoint. If the suitable pooling configuration is unclear, share the configuration type with support before changing it. Never send the database password or a full connection string containing credentials.

Related: [Supabase](https://docs.jetadmin.io/user-guide/data-sources/databases/supabase).

## SQL queries and filters

Compare the query's result with the component's filters and input values in a test page or environment. Use an account with the intended permissions.

A SQL `WHERE` clause may be intentional. Do not remove it merely because a filtered table fails, particularly if it restricts which records a user may see. If a query works but the filtered component fails, send support both configurations and the exact error.

For changed source schemas, see [A data resource is failing to sync](a-data-resource-is-failing-to-sync.md). Review the effect of any schema recreation on your app before proceeding.

## Network, VPN, and self-hosted connections

A VPN, proxy, or firewall can affect connectivity. Compare behavior on another approved network if your organization's policy permits it. Do not disable required security controls.

For self-hosted deployments, review [Jet Bridge common problems](https://docs.jetadmin.io/jet-bridge-deployment/cloud-jet-bridge-and-on-premises/jet-admin/common-problems) for HTTPS and proxy-specific diagnostics.

## What to send support

Use the Jet Admin chat and include:

* App URL and environment.
* Exact error, timestamp, and timezone.
* Affected page, component, query, or automation.
* Steps to reproduce and when it last worked.
* Whether other users or pages are affected.
* A sanitized screenshot or relevant error-log excerpt.

Remove credentials, tokens, and customer data from examples. After a fix, retest the original failing action and the intended user's access.

_Last reviewed: September 16, 2026._
