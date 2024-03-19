---
description: In this section you will learn about Custom SSO OAuth 2.0
---

# Custom SSO OAuth 2.0

Apart from a number of pre-built SSO providers we support integrating with fully Custom [OAuth 2.0](https://oauth.net/2/) compatible providers.&#x20;

The process is not automatic:&#x20;

* First you need to implement OAuth2 flow on your side and make sure it works. You should implement three types of requests for it listed below.&#x20;
* Any SSO integrations require you to [connect your custom domain](../../project-settings/configuring-a-custom-domain.md).
* Contact our tech engineers to test and finish integration on our side. OAuth implementation can vary from provider to provider so we implemented ability to customize OAuth requests used in integration (HTTP method, JSON/Form data, Scope separator, etc.). Our engineers will adapt to your implementation during integration process, but we recommend to stick to the most popular industry implementations (preferable to use open source implementations for your tech stack).

These are global parameters generated on your side

* **CLIENT\_ID** - You apps client id used to identify Jet Admin requests (passed public)
* **CLIENT\_SECRET** - You apps client secret used by Jet Admin to perform requests (stored internally)
* **SCOPE** - (optional) If your backend requires **access\_token** to have list of scopes to make queries this parameter will be used to obtain **access\_token**

### 1. Authorization URL

## Initial page which user is redirected to on Sign In page

<mark style="color:blue;">`GET`</mark> `https://YOUR_SSO_DOMAIN/authorize`

#### Query Parameters

| Name                                             | Type   | Description                                                                                                                                                     |
| ------------------------------------------------ | ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| client\_id<mark style="color:red;">\*</mark>     | String | CLIENT\_ID                                                                                                                                                      |
| state<mark style="color:red;">\*</mark>          | String | Special OAuth2 generated code, created on Jet Admin side                                                                                                        |
| redirect\_uri<mark style="color:red;">\*</mark>  | String | <p>ex. https://api.jetadmin.io/complete/custom_oauth_2/<br>Should be as specified here, you can validate it on your side (optionally)</p>                       |
| response\_type<mark style="color:red;">\*</mark> | String | code                                                                                                                                                            |
| scope<mark style="color:red;">\*</mark>          | String | <p>ex. "openid profile offline_access"<br>Depends on your implementation, should be minimal scope needed to get user profile (first name, last name, email)</p> |

{% hint style="info" %}
If you have only 1 sign in method (SSO) user will be automatically redirected to your SSO initial page without seeing Jet Admin.
{% endhint %}

After Sign In process user will be redirected back to **Jet Admin** side.

## Page that processes received "code" and performs step 2.&#x20;

<mark style="color:blue;">`GET`</mark> `https://api.jetadmin.io/complete/custom_oauth_2/`

#### Query Parameters

| Name                                     | Type   | Description                                                    |
| ---------------------------------------- | ------ | -------------------------------------------------------------- |
| state<mark style="color:red;">\*</mark>  | String | Special OAuth2 generated code, created on Jet Admin side       |
| code<mark style="color:red;">\*</mark>   | String | Special OAuth2 generated code, created on Custom provider side |
| scope<mark style="color:red;">\*</mark>  | String | Previously received scope                                      |
| prompt<mark style="color:red;">\*</mark> | String | consent                                                        |
| authuser                                 | String | 0                                                              |

### 2. Access token URL

## The method is called by Jet Admin backend to get "access" and "refresh" tokens

<mark style="color:green;">`POST`</mark> `https://YOUR_SSO_DOMAIN/token`

#### Request Body

| Name                                             | Type   | Description                                                    |
| ------------------------------------------------ | ------ | -------------------------------------------------------------- |
| grant\_type<mark style="color:red;">\*</mark>    | String | authorization\_code                                            |
| code<mark style="color:red;">\*</mark>           | String | Special OAuth2 generated code, created on Custom provider side |
| client\_id                                       | String | CLIENT\_ID                                                     |
| client\_secret<mark style="color:red;">\*</mark> | String | CLIENT\_SECRET                                                 |
| redirect\_uri<mark style="color:red;">\*</mark>  | String | https://api.jetadmin.io/complete/custom\_oauth\_2/             |

{% tabs %}
{% tab title="200: OK " %}
```javascript
{
    'token_type': 'Bearer',
    'access_token': 'ya29.A0ARrdaM9Hc_Hz__EhytWaIlHcYGkaszuxgKVqeEWBfErtEbHOPRF2_YtvlSY5qbkW2ZKbvbCNPtxGJJHutBsWd2hfmE8ZCdRX0bpQw5iwDfTBJZjQ7S9kKRiiCR165DyLs8hnERkjd3Z8-1-hPSt1X9MrY8aX',
    'expires_in': 3599, 
    'refresh_token': '1//09uFin2WWZE9gCgYIARAAGAkSNwF-L9Irrrh5VtbNA35jfyWv8xnrj-VSqMKwCP-yjKtP6h6IDA6A0-S-LgqGve9Z-RLZzFdZpaE',
    'scope': 'openid profile offline_access'
}
```
{% endtab %}
{% endtabs %}

**access\_token** JWT payload should have fields:&#x20;

* first\_name
* last\_name (optional)
* username (can be equal to email)
* email

**access token** and **refresh token** obtained on this step are saved on api.jetadmin.io side.&#x20;

{% hint style="info" %}
(optional) If you have self-hosted Jet Bridge set up as [HTTP proxy](../../../jet-bridge-deployment/jet-admin/using-self-deployed-http-proxy.md) access token and refresh token can be saved on self-hosted Jet Bridge side.&#x20;
{% endhint %}

### 3. Refresh token URL

Can be the same as Access token URL, but with different data

## The method is called by Jet Admin backend to refresh expired "access token"

<mark style="color:green;">`POST`</mark> `https://YOUR_SSO_DOMAIN/token`

#### Request Body

| Name                                             | Type   | Description    |
| ------------------------------------------------ | ------ | -------------- |
| grant\_type<mark style="color:red;">\*</mark>    | String | refresh\_token |
| refresh\_token<mark style="color:red;">\*</mark> | String |                |
| client\_id                                       | String | CLIENT\_ID     |
| client\_secret<mark style="color:red;">\*</mark> | String | CLIENT\_SECRET |

{% tabs %}
{% tab title="200: OK " %}
```javascript
{
    'token_type': 'Bearer',
    'access_token': 'ya29.A0ARrdaM9Hc_Hz__EhytWaIlHcYGkaszuxgKVqeEWBfErtEbHOPRF2_YtvlSY5qbkW2ZKbvbCNPtxGJJHutBsWd2hfmE8ZCdRX0bpQw5iwDfTBJZjQ7S9kKRiiCR165DyLs8hnERkjd3Z8-1-hPSt1X9MrY8aX',
    'expires_in': 3599, 
    'refresh_token': '1//09uFin2WWZE9gCgYIARAAGAkSNwF-L9Irrrh5VtbNA35jfyWv8xnrj-VSqMKwCP-yjKtP6h6IDA6A0-S-LgqGve9Z-RLZzFdZpaE', 
    'scope': 'openid profile offline_access'
}
```
{% endtab %}
{% endtabs %}



### Authorizing API calls to your backend with SSO token

{% content-ref url="api-calls-with-sso-token.md" %}
[api-calls-with-sso-token.md](api-calls-with-sso-token.md)
{% endcontent-ref %}
