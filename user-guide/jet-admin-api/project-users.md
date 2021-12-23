# Users API

{% swagger baseUrl="https://api.jetadmin.io" path="/api/projects/:PROJECT_NAME/users/" method="get" summary="Get list of all project users" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="PROJECT_NAME" type="string" %}
Unique project name (can be taken from Jet Admin project URL)
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
Token authentication, example: 

\




`Authorization: ProjectToken f42a3cab3f146b283701a4e314f1c7ba57fdb59e`
{% endswagger-parameter %}

{% swagger-parameter in="query" name="_paginate" type="number" %}
Return response as pages (0 or 1)
{% endswagger-parameter %}

{% swagger-parameter in="query" name="search" type="string" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Default" %}
```javascript
{
    id: 1504,
    user: {
        username: "a.svetlov@geex-arts.com"
        first_name: "Anton"
        last_name: "Svetlov"
        email: "a.svetlov@geex-arts.com"
        photo: "https://api.jetadmin.io/media/user/photo/2018/10/09/18402150_1144874585658871_7416256167591393723_o.jpg"
        uid: "28c9bc6d-1f80-4898-93d3-154fa66b22ac"
    },
    user_email: null
    group: {
        id: 1491
        name: "Administrators"
        description: ""
        super_group: true
        project_permissions: []
        properties: {}
    },
    properties: {
        office: "Dubai"
    },
    date_add: "2018-09-30T16:58:52.067471+03:00"
}
```
{% endswagger-response %}

{% swagger-response status="200: OK" description="Paginated" %}
```javascript
{
   "count":1,
   "next":null,
   "previous":null,
   "results":[
      {
         "id":1504,
         "user":{
            "username":"a.svetlov@geex-arts.com",
            "first_name":"Anton",
            "last_name":"Svetlov",
            "email":"a.svetlov@geex-arts.com",
            "photo":"https://api.jetadmin.io/media/user/photo/2018/10/09/18402150_1144874585658871_7416256167591393723_o.jpg",
            "uid":"28c9bc6d-1f80-4898-93d3-154fa66b22ac"
         },
         "user_email":null,
         "group":{
            "id":1491,
            "name":"Administrators",
            "description":"",
            "super_group":true,
            "project_permissions":[
               
            ],
            "properties":{
               
            }
         },
         "properties":{
            "office":"Dubai"
         },
         "date_add":"2018-09-30T16:58:52.067471+03:00"
      }
   ]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://api.jetadmin.io" path="/api/projects/:PROJECT_NAME/users/" method="post" summary="Invite new project user and send invite" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="PROJECT_NAME" type="string" %}
Unique project name (can be taken from Jet Admin project URL)
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
Token authentication, example: 

\




`Authorization: ProjectToken f42a3cab3f146b283701a4e314f1c7ba57fdb59e`
{% endswagger-parameter %}

{% swagger-parameter in="body" name="user_email" type="string" %}
User email, example: a.svetlov@geex-arts.com
{% endswagger-parameter %}

{% swagger-parameter in="body" name="group" type="number" %}
Group ID, example: 1491
{% endswagger-parameter %}

{% swagger-parameter in="body" name="properties" type="object" %}
JSON Object, example: {office: "New York"}
{% endswagger-parameter %}

{% swagger-response status="201" description="" %}
```javascript
{
    id: 1504,
    user_email: null
    group: 1491,
    properties: {
        office: "Dubai"
    },
    date_add: "2018-09-30T16:58:52.067471+03:00"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://api.jetadmin.io" path="/api/projects/:PROJECT_NAME/users/:USER_ID/" method="patch" summary="Update existing project user" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="PROJECT_NAME" type="string" %}
Unique project name (can be taken from Jet Admin project URL)
{% endswagger-parameter %}

{% swagger-parameter in="path" name="USER_ID" type="number" %}
Project user ID
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
Token authentication, example: 

\




`Authorization: ProjectToken f42a3cab3f146b283701a4e314f1c7ba57fdb59e`
{% endswagger-parameter %}

{% swagger-parameter in="body" name="user_email" type="string" %}
User email, example: a.svetlov@geex-arts.com
{% endswagger-parameter %}

{% swagger-parameter in="body" name="group" type="number" %}
Group ID, example: 1491
{% endswagger-parameter %}

{% swagger-parameter in="body" name="properties" type="object" %}
JSON Object, example: {office: "New York"}
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```javascript
{
    id: 1504,
    user_email: null
    group: 1491,
    properties: {
        office: "Dubai"
    },
    date_add: "2018-09-30T16:58:52.067471+03:00"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://api.jetadmin.io" path="/api/projects/:PROJECT_NAME/users/:USER_ID/" method="delete" summary="Delete existing project user" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="PROJECT_NAME" type="string" %}
Unique project name (can be taken from Jet Admin project URL)
{% endswagger-parameter %}

{% swagger-parameter in="path" name="USER_ID" type="number" %}
Project user ID
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
Token authentication, example: 

\




`Authorization: ProjectToken f42a3cab3f146b283701a4e314f1c7ba57fdb59e`
{% endswagger-parameter %}

{% swagger-response status="204" description="" %}
```
```
{% endswagger-response %}
{% endswagger %}

## For projects with multiple environments

{% swagger baseUrl="https://api.jetadmin.io" path="/api/projects/:PROJECT_NAME/:ENVIRONMENT_NAME/users/" method="get" summary="Get list of all project environment users" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="ENVIRONMENT_NAME" type="string" %}
Environment name in URL
{% endswagger-parameter %}

{% swagger-parameter in="path" name="PROJECT_NAME" type="string" %}
Unique project name (can be taken from Jet Admin project URL)
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
Token authentication, example: 

\




`Authorization: ProjectToken f42a3cab3f146b283701a4e314f1c7ba57fdb59e`
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```javascript
{
    id: 1504,
    user: {
        username: "a.svetlov@geex-arts.com"
        first_name: "Anton"
        last_name: "Svetlov"
        email: "a.svetlov@geex-arts.com"
        photo: "https://api.jetadmin.io/media/user/photo/2018/10/09/18402150_1144874585658871_7416256167591393723_o.jpg"
        uid: "28c9bc6d-1f80-4898-93d3-154fa66b22ac"
    },
    user_email: null
    group: {
        id: 1491
        name: "Administrators"
        description: ""
        super_group: true
        project_permissions: []
        properties: {}
    },
    properties: {
        office: "Dubai"
    },
    date_add: "2018-09-30T16:58:52.067471+03:00"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://api.jetadmin.io" path="/api/projects/:PROJECT_NAME/:ENVIRONMENT_NAME/users/" method="post" summary="Invite new project environment user and send invite" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="ENVIRONMENT_NAME" type="string" %}
Environment name in URL
{% endswagger-parameter %}

{% swagger-parameter in="path" name="PROJECT_NAME" type="string" %}
Unique project name (can be taken from Jet Admin project URL)
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
Token authentication, example: 

\




`Authorization: ProjectToken f42a3cab3f146b283701a4e314f1c7ba57fdb59e`
{% endswagger-parameter %}

{% swagger-parameter in="body" name="user_email" type="string" %}
User email, example: a.svetlov@geex-arts.com
{% endswagger-parameter %}

{% swagger-parameter in="body" name="group" type="number" %}
Group ID, example: 1491
{% endswagger-parameter %}

{% swagger-parameter in="body" name="properties" type="object" %}
JSON Object, example: {office: "New York"}
{% endswagger-parameter %}

{% swagger-response status="201" description="" %}
```javascript
{
    id: 1504,
    user_email: null
    group: 1491,
    properties: {
        office: "Dubai"
    },
    date_add: "2018-09-30T16:58:52.067471+03:00"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://api.jetadmin.io" path="/api/projects/:PROJECT_NAME/:ENVIRONMENT_NAME/users/:USER_ID/" method="patch" summary="Update existing project environment user" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="ENVIRONMENT_NAME" type="string" %}
Environment name in URL
{% endswagger-parameter %}

{% swagger-parameter in="path" name="PROJECT_NAME" type="string" %}
Unique project name (can be taken from Jet Admin project URL)
{% endswagger-parameter %}

{% swagger-parameter in="path" name="USER_ID" type="number" %}
Project user ID
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
Token authentication, example: 

\




`Authorization: ProjectToken f42a3cab3f146b283701a4e314f1c7ba57fdb59e`
{% endswagger-parameter %}

{% swagger-parameter in="body" name="user_email" type="string" %}
User email, example: a.svetlov@geex-arts.com
{% endswagger-parameter %}

{% swagger-parameter in="body" name="group" type="number" %}
Group ID, example: 1491
{% endswagger-parameter %}

{% swagger-parameter in="body" name="properties" type="object" %}
JSON Object, example: {office: "New York"}
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```javascript
{
    id: 1504,
    user_email: null
    group: 1491,
    properties: {
        office: "Dubai"
    },
    date_add: "2018-09-30T16:58:52.067471+03:00"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://api.jetadmin.io" path="/api/projects/:PROJECT_NAME/:ENVIRONMENT_NAME/users/:USER_ID/" method="delete" summary="Delete existing project environment user" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="ENVIRONMENT_NAME" type="string" %}
Environment name in URL
{% endswagger-parameter %}

{% swagger-parameter in="path" name="PROJECT_NAME" type="string" %}
Unique project name (can be taken from Jet Admin project URL)
{% endswagger-parameter %}

{% swagger-parameter in="path" name="USER_ID" type="number" %}
Project user ID
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
Token authentication, example: 

\




`Authorization: ProjectToken f42a3cab3f146b283701a4e314f1c7ba57fdb59e`
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
```
{% endswagger-response %}
{% endswagger %}
