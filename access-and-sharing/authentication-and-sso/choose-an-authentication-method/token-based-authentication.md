# Token-based authentication

Use this integration checklist when your application already has a custom authentication flow or needs to pass a user's identity to an API.

There is no single token configuration that applies to every provider. Confirm the supported integration path before implementation.

## Choose the intended behavior

| Need                                    | Related guide                                                              |
| --------------------------------------- | -------------------------------------------------------------------------- |
| Sign users in through an OAuth provider | [Custom SSO OAuth 2.0](../sign-in-sign-up/custom-sso-oauth-2.0.md)         |
| Make API requests with an SSO token     | [API calls with SSO token](../sign-in-sign-up/api-calls-with-sso-token.md) |
| Authenticate users with Xano            | [Xano Auth](xano-auth.md)                                                  |

The current External Authentication selector also includes **Custom authentication**. Its configuration must match the actual identity service and the fields in its setup form.

## Define and test the contract

Document the token issuer, intended API or audience, expiration behavior, identity mapping, and how the API validates requests. The API must decide whether that identity may perform the requested action on the requested record.

Test missing, invalid, expired, and wrong-user credentials as well as a successful request. Check that signing out and removing access have the behavior your application requires.

Do not place production tokens in example URLs, screenshots, prompts, or shared logs. For application data access, follow [Restrict access to records](../../app-and-data-permissions/record-access.md).
