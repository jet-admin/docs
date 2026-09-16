---
description: In this section you will learn how to build Sign In/Sign Up Page
icon: shield-keyhole
---

# App SSO

Connect your app to an external identity provider using the protocol supported by your organization.

## Provider guides

| Provider           | Setup guide                                                      |
| ------------------ | ---------------------------------------------------------------- |
| Auth0              | [OAuth 2.0](auth0-sso-oauth-2.0.md) or [SAML2](auth0-sso.md)     |
| Microsoft Azure AD | [OAuth 2.0](auth0-sso-oauth-2.0-1.md)                            |
| Okta               | [Okta SSO](okta-sso.md)                                          |
| Google             | [OAuth 2.0](google-oauth-2.0.md) or [SAML2](google-sso-saml2.md) |
| Custom provider    | [OAuth 2.0](custom-sso-oauth-2.0.md)                             |

## Start in the current builder

Open **More → Authentication → Add External Authentication**, then select the appropriate provider. Existing provider tutorials may show earlier navigation and identity-provider screens; use the values displayed in your current configuration.

Confirm the app environment, redirect or callback values, identity mapping, and team assignment before rollout. Test successful sign-in and rejection of an unintended account, while retaining a working administrator sign-in path.

If your API needs the authenticated user's token, see [API calls with SSO token](api-calls-with-sso-token.md).

## Classic sign-in page customization

The earlier sign-in page editor offered visual customization for login and signup screens. That workflow is separate from configuring an identity provider. Use the authentication settings above for the current builder.

If sign-in or redirects fail, continue with [Troubleshoot sign-in](../troubleshoot-sign-in.md).
