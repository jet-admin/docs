---
description: >-
  This guide provides step-by-step instructions on integrating Supabase into
  JetAdmin for creating a unified authentication system.
---

# Supabase Auth

## Pre-requisites

* **Supabase Account**: Ensure you have an active Supabase account.
* **JetAdmin Account**: Similarly, a JetAdmin account is required. [Register](https://app.jetadmin.io/projects/create) if you haven't already.
* **User Table in Supabase**: Set up a user table in your Supabase project. It is located at "**Authentication" -> "Users"**

## Setting up custom authentication

This example demonstrates how to add user authentication to JetAdmin with Supabase. In this scenario, access management is performed on the JetAdmin side.

1. Create a new External Auth Method and select "Supabase auth"
2. Customize the name and icon (Optional)
3. Select to which team users are going to be assigned to
4. Paste your "Reference ID" and "API Key" from Supabase
5. Save changes

{% @arcade/embed flowId="YQFeTmwct0rkfkcrogup" url="https://app.arcade.software/share/YQFeTmwct0rkfkcrogup" %}

## Changing the sign-up page appearance

* Publish your changes if you haven't already
* Disable/enable those methods that you are planning to use
* Check whether the preview is displaying everything correctly
* Customize names and icons for your external auth methods

{% @arcade/embed flowId="8q7oiiZJEwerK1rZ9quP" url="https://app.arcade.software/share/8q7oiiZJEwerK1rZ9quP" %}

## Testing the sign-in flow

1. Open up a separate browser instance
2. Navigate to the sign-in page and try to log in using test credentials
3. Check whether you are signed and have appropriate access
4. Get back to your admin panel and check whether the user was created in JetAdmin
