---
icon: lock
---

# Authentication and SSO

Choose how users prove their identity, then test the access they receive after sign-in.

Open **More → Authentication** in the builder, or use the **Authentication** tab in the Users area.

![Authentication settings with Built-in and External Authentication sections](../../.gitbook/assets/07-authentication.png)

## Choose your path

* [Jet Auth and built-in sign-in](choose-an-authentication-method/jet-auth-and-built-in-sign-in.md) — review the built-in options.
* [Choose an authentication method](choose-an-authentication-method/) — compare built-in and external authentication.
* [App SSO](sign-in-sign-up/) — use the existing provider-specific setup guides.
* [Troubleshoot sign-in](troubleshoot-sign-in.md) — investigate login or redirect failures.

The External Authentication selector includes Firebase Auth, Supabase Auth, and OAuth providers. The exact provider configuration depends on the selected method.

## Finish configuration with a test

Keep a working administrator sign-in available while testing a new method. Use a separate intended test account to verify sign-in, identity, team assignment, and access to the published app.

Authentication and authorization are separate: a valid identity should only receive the permissions you intended. Continue with [the access test checklist](../overview/test-access.md).
