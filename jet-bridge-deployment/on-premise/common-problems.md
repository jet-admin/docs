# Common Problems

### Requests to API are being rejected by not using HTTPS <a href="#https-issue" id="https-issue"></a>

Currently there is no built-it **SSL** support in on-premise package, so you should add an **NGINX or other web server** with **SSL** in front of **Docker** instance which will proxy requests to Docker instance. This is planned to be added in future as a built-it functionality.

### Forbidden error when connecting to self-hosted Jet Bridge <a href="#https-issue" id="https-issue"></a>

**Jet Bridge** package include **JWT\_VERIFY\_TOKEN** inside it to verify requests from the frontend. By default it uses our Cloud **JWT\_VERIFY\_TOKEN**, but for on-premise you have different JWT key pair (randomly generated on install) so you need to change it. You should make it equals to the **JWT\_VERIFY\_KEY** value in your on-premise package config.

```
# Jet Bridge setting
JWT_VERIFY_KEY=-----BEGIN PUBLIC KEY-----\nMIICIjANBgkqhkiG9w0BAQEFAAOC...

# If using Jet Bridge for Django
JET_JWT_VERIFY_KEY=-----BEGIN PUBLIC KEY-----\nMIICIjANBgkqhkiG9w0BAQEFAAOC...
```

{% hint style="info" %}
You you can learn more about Jet Bridge configuration [here](../jet-admin/configuration.md)
{% endhint %}
