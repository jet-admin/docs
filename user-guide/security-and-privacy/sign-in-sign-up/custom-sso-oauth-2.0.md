# Custom SSO OAuth 2.0

Apart from a number of pre-built SSO providers we support integrating with fully Custom OAuth 2.0 compatible providers. You should implement three types for requests for it.

These are global parameters generated in your side

* **CLIENT\_ID** - You apps client id used to identify Jet Admin requests (passed public)
* **CLIENT\_SECRET** - You apps client secret used by Jet Admin to perform requests (stored internally)

### 1. Authorization URL

{% swagger method="get" path="/authorize" baseUrl="https://YOUR_SSO_DOMAIN" summary="Initial page which user is redirected to Sign In" %}
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



{% swagger method="get" path="/complete/custom_oauth_2/" baseUrl="https://api.jetadmin.io" summary="After Sign In process user should be redirected here" %}
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

{% swagger method="post" path="/token" baseUrl="https://YOUR_SSO_DOMAIN" summary="The method is called by Jet Admin backend to get Access and Refresh tokens" %}
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
    'refresh_token': '1//09uFin2WWZE9gCgYIARAAGAkSNwF-L9Irrrh5VtbNA35jfyWv8xnrj-VSqMKwCP-yjKtP6h6IDA6A0-S-LgqGve9Z-RLZzFdZpaE', 'scope': 'openid https://www.googleapis.com/auth/userinfo.profile https://www.googleapis.com/auth/userinfo.email', 
    'id_token': 'eyJhbGciOiJSUzI1NiIsImtpZCI6ImNlYzEzZGViZjRiOTY0Nzk2ODM3MzYyMDUwODI0NjZjMTQ3OTdiZDAiLCJ0eXAiOiJKV1QifQ.eyJpc3MiOiJhY2NvdW50cy5nb29nbGUuY29tIiwiYXpwIjoiMzcxODQ5NDAyMTA3LTg4OWRnY3JkcGt0a2Q5NmhlNWZpN3N2aDZsYmxzMzc2LmFwcHMuZ29vZ2xldXNlcmNvbnRlbnQuY29tIiwiYXVkIjoiMzcxODQ5NDAyMTA3LTg4OWRnY3JkcGt0a2Q5NmhlNWZpN3N2aDZsYmxzMzc2LmFwcHMuZ29vZ2xldXNlcmNvbnRlbnQuY29tIiwic3ViIjoiMTA4ODk1NjAyOTA1Njc4NjU1Njc3IiwiZW1haWwiOiJkZW5raWw5MkBnbWFpbC5jb20iLCJlbWFpbF92ZXJpZmllZCI6dHJ1ZSwiYXRfaGFzaCI6Im4yTHRfVGFBeXhhSTlyX2NHLVkzRmciLCJpYXQiOjE2NDk0MTU0NDMsImV4cCI6MTY0OTQxOTA0M30.fVinxrR9dDT8ArhkdQNxZPYduxPYSFPxFC-9I3fvrUZ0GCxdRadyYzeXqgEcLuONF8DCTVJDegIFikmN7j3iyq6YekxVWgAh6v3D9xIJXuRQhpdIEFpTxEa7kibruYGjELudCJyQ4QLMF5ROteLOKfbgeqa_jOiU6I10dXVdHIQMsJCJwIaFB7BHX4TyrSDxKjr_DJqvUeKILp8lyA-OLz4eSNlTAlWCZKaNijQf5snzLtaKOcKqBQLRVapfqNCLIHAZXV7abuxGjQc413QCsLiXX-WgBLzlbVjpN4Pqv93Hp2clq9eIrz7TLDy64KUHCwtLq-M4PW5On_JLO12eBw'
}
```
{% endswagger-response %}
{% endswagger %}

**access\_token** JWT payload should have fields:&#x20;

* first\_name
* last\_name (optional)
* username (can be equal to email)
* email

### 3. Refresh token URL

Can be the same as Access token URL, but with different data

{% swagger method="post" path="/token" baseUrl="https://YOUR_SSO_DOMAIN" summary="The method is called by Jet Admin backend to refresh expired Access token" %}
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
    'refresh_token': '1//09uFin2WWZE9gCgYIARAAGAkSNwF-L9Irrrh5VtbNA35jfyWv8xnrj-VSqMKwCP-yjKtP6h6IDA6A0-S-LgqGve9Z-RLZzFdZpaE', 'scope': 'openid https://www.googleapis.com/auth/userinfo.profile https://www.googleapis.com/auth/userinfo.email', 
    'id_token': 'eyJhbGciOiJSUzI1NiIsImtpZCI6ImNlYzEzZGViZjRiOTY0Nzk2ODM3MzYyMDUwODI0NjZjMTQ3OTdiZDAiLCJ0eXAiOiJKV1QifQ.eyJpc3MiOiJhY2NvdW50cy5nb29nbGUuY29tIiwiYXpwIjoiMzcxODQ5NDAyMTA3LTg4OWRnY3JkcGt0a2Q5NmhlNWZpN3N2aDZsYmxzMzc2LmFwcHMuZ29vZ2xldXNlcmNvbnRlbnQuY29tIiwiYXVkIjoiMzcxODQ5NDAyMTA3LTg4OWRnY3JkcGt0a2Q5NmhlNWZpN3N2aDZsYmxzMzc2LmFwcHMuZ29vZ2xldXNlcmNvbnRlbnQuY29tIiwic3ViIjoiMTA4ODk1NjAyOTA1Njc4NjU1Njc3IiwiZW1haWwiOiJkZW5raWw5MkBnbWFpbC5jb20iLCJlbWFpbF92ZXJpZmllZCI6dHJ1ZSwiYXRfaGFzaCI6Im4yTHRfVGFBeXhhSTlyX2NHLVkzRmciLCJpYXQiOjE2NDk0MTU0NDMsImV4cCI6MTY0OTQxOTA0M30.fVinxrR9dDT8ArhkdQNxZPYduxPYSFPxFC-9I3fvrUZ0GCxdRadyYzeXqgEcLuONF8DCTVJDegIFikmN7j3iyq6YekxVWgAh6v3D9xIJXuRQhpdIEFpTxEa7kibruYGjELudCJyQ4QLMF5ROteLOKfbgeqa_jOiU6I10dXVdHIQMsJCJwIaFB7BHX4TyrSDxKjr_DJqvUeKILp8lyA-OLz4eSNlTAlWCZKaNijQf5snzLtaKOcKqBQLRVapfqNCLIHAZXV7abuxGjQc413QCsLiXX-WgBLzlbVjpN4Pqv93Hp2clq9eIrz7TLDy64KUHCwtLq-M4PW5On_JLO12eBw'
}
```
{% endswagger-response %}
{% endswagger %}
