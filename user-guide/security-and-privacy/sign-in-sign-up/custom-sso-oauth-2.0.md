# Custom SSO OAuth 2.0

Apart from a number of pre-built SSO providers we support integrating with fully Custom [OAuth 2.0](https://oauth.net/2/) compatible providers.&#x20;

The process is not automatic:&#x20;

* First you need to implement OAuth2 flow on your side and make sure it works. You should implement three types of requests for it listed below.&#x20;
* Any SSO integrations require you to [connect your custom domai](../../project-settings/configuring-a-custom-domain.md)n.
* Contact our tech engineers to test and finish integration on our side. OAuth implementation can vary from provider to provider so we implemented ability to customize OAuth requests used in integration (HTTP method, JSON/Form data, Scope separator, etc.). Our engineers will adapt to your implementation during integration process, but we recommend to stick to the most popular industry implementations (preferable to use open source implementations for your tech stack).

These are global parameters generated on your side

* **CLIENT\_ID** - You apps client id used to identify Jet Admin requests (passed public)
* **CLIENT\_SECRET** - You apps client secret used by Jet Admin to perform requests (stored internally)
* **SCOPE** - (optional) If your backend requires **access\_token** to have list of scopes to make queries this parameter will be used to obtain **access\_token**

### 1. Authorization URL

{% swagger method="get" path="/authorize" baseUrl="https://YOUR_SSO_DOMAIN" summary="Initial page which user is redirected to on Sign In page" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="client_id" required="true" %}
CLIENT_ID
{% endswagger-parameter %}

{% swagger-parameter in="query" name="state" required="true" %}
Special OAuth2 generated code, created on Jet Admin side
{% endswagger-parameter %}

{% swagger-parameter in="query" name="redirect_uri" required="true" %}
ex. https://api.jetadmin.io/complete/custom_oauth_2/

\


Should be as specified here, you can validate it on your side (optionally)
{% endswagger-parameter %}

{% swagger-parameter in="query" name="response_type" required="true" %}
code
{% endswagger-parameter %}

{% swagger-parameter in="query" name="scope" required="true" %}
ex. "openid profile offline_access"

\


Depends on your implementation, should be minimal scope needed to get user profile (first name, last name, email)
{% endswagger-parameter %}
{% endswagger %}

{% hint style="info" %}
If you have only 1 sign in method (SSO) user will be automatically redirected to your SSO initial page without seeing Jet Admin.
{% endhint %}

After Sign In process user will be redirected back to **Jet Admin** side.

{% swagger method="get" path="/complete/custom_oauth_2/" baseUrl="https://api.jetadmin.io" summary="Page that processes received "code" and performs step 2. " %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="state" required="true" %}
Special OAuth2 generated code, created on Jet Admin side
{% endswagger-parameter %}

{% swagger-parameter in="query" name="code" required="true" %}
Special OAuth2 generated code, created on Custom provider side
{% endswagger-parameter %}

{% swagger-parameter in="query" name="scope" required="true" %}
Previously received scope
{% endswagger-parameter %}

{% swagger-parameter in="query" name="prompt" required="true" %}
consent
{% endswagger-parameter %}

{% swagger-parameter in="query" name="authuser" %}
0
{% endswagger-parameter %}
{% endswagger %}

### 2. Access token URL

{% swagger method="post" path="/token" baseUrl="https://YOUR_SSO_DOMAIN" summary="The method is called by Jet Admin backend to get "access" and "refresh" tokens" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="grant_type" required="true" %}
authorization_code
{% endswagger-parameter %}

{% swagger-parameter in="body" name="code" required="true" %}
Special OAuth2 generated code, created on Custom provider side
{% endswagger-parameter %}

{% swagger-parameter in="body" name="client_id" %}
CLIENT_ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="client_secret" required="true" %}
CLIENT_SECRET
{% endswagger-parameter %}

{% swagger-parameter in="body" name="redirect_uri" required="true" %}
https://api.jetadmin.io/complete/custom_oauth_2/
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    'token_type': 'Bearer',
    'access_token': 'ya29.A0ARrdaM9Hc_Hz__EhytWaIlHcYGkaszuxgKVqeEWBfErtEbHOPRF2_YtvlSY5qbkW2ZKbvbCNPtxGJJHutBsWd2hfmE8ZCdRX0bpQw5iwDfTBJZjQ7S9kKRiiCR165DyLs8hnERkjd3Z8-1-hPSt1X9MrY8aX',
    'expires_in': 3599, 
    'refresh_token': '1//09uFin2WWZE9gCgYIARAAGAkSNwF-L9Irrrh5VtbNA35jfyWv8xnrj-VSqMKwCP-yjKtP6h6IDA6A0-S-LgqGve9Z-RLZzFdZpaE',
    'scope': 'openid profile offline_access'
}
```
{% endswagger-response %}
{% endswagger %}

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

{% swagger method="post" path="/token" baseUrl="https://YOUR_SSO_DOMAIN" summary="The method is called by Jet Admin backend to refresh expired "access token"" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="grant_type" required="true" %}
refresh_token
{% endswagger-parameter %}

{% swagger-parameter in="body" name="refresh_token" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="client_id" %}
CLIENT_ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="client_secret" required="true" %}
CLIENT_SECRET
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    'token_type': 'Bearer',
    'access_token': 'ya29.A0ARrdaM9Hc_Hz__EhytWaIlHcYGkaszuxgKVqeEWBfErtEbHOPRF2_YtvlSY5qbkW2ZKbvbCNPtxGJJHutBsWd2hfmE8ZCdRX0bpQw5iwDfTBJZjQ7S9kKRiiCR165DyLs8hnERkjd3Z8-1-hPSt1X9MrY8aX',
    'expires_in': 3599, 
    'refresh_token': '1//09uFin2WWZE9gCgYIARAAGAkSNwF-L9Irrrh5VtbNA35jfyWv8xnrj-VSqMKwCP-yjKtP6h6IDA6A0-S-LgqGve9Z-RLZzFdZpaE', 
    'scope': 'openid profile offline_access'
}
```
{% endswagger-response %}
{% endswagger %}

### Authorization of API calls to your backend with SSO token

When user is logged in with **SSO** it is possible to use **SSO access token** in **HTTP** queries (**Rest API** or **GraphQL**). Such requests are going through api.jetadmin.io endpoint or self-hosted **Jet Bridge** (when set up as [HTTP proxy](../../../jet-bridge-deployment/jet-admin/using-self-deployed-http-proxy.md)).

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (2).png" alt=""><figcaption></figcaption></figure>
