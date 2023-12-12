---
description: In this section you will learn how the SSO authentication flow can be done
---

# SSO on self-deployed Jet Bridge

If want SSO authentication flow to be done on your side you can configure Jet Bridge to process SSO authentication. It will also save the SSO provider's access tokens on the Jet Bridge side in cookies (instead of app.jetadmin.io by default).

#### 1. Deploy standalone Jet Bridge as described here

{% content-ref url="using-self-deployed-http-proxy.md" %}
[using-self-deployed-http-proxy.md](using-self-deployed-http-proxy.md)
{% endcontent-ref %}

#### 2. Change SSO Application type to Jet Bridge and specify Jet Bridge URL

![](<../../.gitbook/assets/image (589).png>)



#### 3. Set up SSO configuration in Jet Bridge config file/environment

**SSO\_APPLICATIONS** = {"a4f1552c-fdc2-4f56-ae23-6291df36ade4": {"backend\_path": .... \}}

**SSO\_APPLICATIONS** is a JSON serialized dictionary of SSO application settings. \
**Key** is SSO Application ID\
**Value** is a dictionary with credentials

\
Here is an example of its content:

```
{
    "a4f1552c-fdc2-4f56-ae23-6291df36ade4": {
        "backend_path": "social_core.backends.azuread_tenant.AzureADV2TenantOAuth2",
        "key": "5d472cb3-87e6-446e-a94f-72e15880c9ce",
        "scope": ["profile", "offline_access"],
        "secret": "nWSt.YG120a_1f.Wz-01TtZ2m-P4YeL3B0",
        "tenant_id": "abbc4033-e302-4eb6-b3ce-57c4f0e4956c",
        "scope_separator": " "
    }
}
```

Required parameters are **backend\_path**, **key**, **secret.** Other parameters are optional and depend on the selected SSO provider.'

#### 4. (optional) Make sure Allow Origin is set correctly in Jet Bridge config and Jet Bridge is working through HTTPS

Settings **ALLOW\_ORIGIN** is required when using a self-deployed HTTP proxy\
Running **Jet Bridge** through **HTTPS** is required if you want to use **SSO access tokens** in requests
