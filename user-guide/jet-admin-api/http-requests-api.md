# HTTP requests API

{% swagger baseUrl="https://" path="api.jetadmin.io/api/proxy_request/" method="post" summary="Send request through Jet Admin proxy" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
JWT eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJ0b2tlbl9Cfb....
{% endswagger-parameter %}

{% swagger-parameter in="body" name="project" type="string" %}
Project unique name
{% endswagger-parameter %}

{% swagger-parameter in="body" name="environment" type="string" %}
Environment unique name (default is prod)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="resource" type="string" %}
Resource unique name
{% endswagger-parameter %}

{% swagger-parameter in="body" name="method" type="string" %}
HTTP method (GET, POST, PUT, PATCH, DELETE, etc.)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="url" type="string" %}
HTTP URL
{% endswagger-parameter %}

{% swagger-parameter in="body" name="query_params" type="array" %}
JSON formatted array, for example:\
\[{"foo":"q","value":"bar"}]
{% endswagger-parameter %}

{% swagger-parameter in="body" name="headers" type="array" %}
JSON formatted array, for example:\
\[{"name":"Authorization","value":"Header {-sso.9b4348ec965d4c68818aec4e15dc536f.access\_token-}"}]&#x20;
{% endswagger-parameter %}

{% swagger-parameter in="body" name="body_type" type="string" %}
Body type (JSON, GraphQL, FormUrlEncoded, FormData, Raw)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="body" type="string" %}
Body depending on selected Body type
{% endswagger-parameter %}

{% swagger-parameter in="body" name="secret_tokens" type="string" %}
Comma separated list of used secret tokens, for example:\
sso.9b4348ec965d4c68818aec4e15dc536f.access\_token
{% endswagger-parameter %}

{% swagger-response status="200" description="Response returned by provided HTTP URL" %}
```
[any data]
```
{% endswagger-response %}
{% endswagger %}
