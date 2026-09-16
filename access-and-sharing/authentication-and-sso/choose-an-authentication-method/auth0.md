# Auth0

Choose the Auth0 guide that matches your organization's authentication protocol.

* [Auth0 with OAuth 2.0](../sign-in-sign-up/auth0-sso-oauth-2.0.md)
* [Auth0 with SAML2](../sign-in-sign-up/auth0-sso.md)

## Before configuration

Confirm which protocol your identity administrator intends to use and which app environment you are configuring. Use the callback, redirect, or service-provider values displayed for that environment.

In the current builder, begin at **More → Authentication → Add External Authentication**. The selector includes **Auth0 OAuth 2.0**. Provider guides may show earlier navigation or provider-console layouts.

## Verify the integration

Test with an intended Auth0 account and check the identity that arrives in Jet Admin, its team assignment, and its access to the published app. Include an account that should not have access.

Keep an existing administrator sign-in available until the new flow is working. If authentication succeeds but the user sees the wrong records or actions, investigate [authorization](../../app-and-data-permissions/) separately from the identity-provider setup.

For errors and redirect loops, use [Troubleshoot sign-in](../troubleshoot-sign-in.md).
