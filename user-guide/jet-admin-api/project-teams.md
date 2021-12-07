# Teams API

{% swagger baseUrl="https://api.jetadmin.io" path="/api/projects/:PROJECT_NAME/groups/" method="get" summary="Get list of all project teams" %}
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

{% swagger-response status="200" description="" %}
```javascript
[
    {
        id: 35091
        name: "Sales"
        description: ""
        super_group: false
        project_permissions: [
            {
                id: 525
                permission_type: "model"
                permission_object: "jet_bridge.users_user"
                permission_actions: "r"
                date_add: "2019-03-22T19:03:02.425689+03:00"
            }
        ],
        properties: {
            industry: "EdTech"
        }
    }
]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://api.jetadmin.io" path="/api/projects/:PROJECT_NAME/groups/" method="post" summary="Create new project team" %}
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

{% swagger-parameter in="body" name="name" type="string" %}
Group name, example: "Sales"
{% endswagger-parameter %}

{% swagger-parameter in="body" name="super_group" type="boolean" %}
If group will have all permissions
{% endswagger-parameter %}

{% swagger-parameter in="body" name="project_permissions" type="array" %}
Array of permissions
{% endswagger-parameter %}

{% swagger-parameter in="body" name="properties" type="object" %}
JSON Object, example: {"industry": "New York"}
{% endswagger-parameter %}

{% swagger-response status="201" description="" %}
```javascript
{
    id: 35091
    name: "Sales"
    description: ""
    super_group: false
    project_permissions: [
        {
            id: 525
            permission_type: "model"
            permission_object: "jet_bridge.users_user"
            permission_actions: "r"
            date_add: "2019-03-22T19:03:02.425689+03:00"
        }
    ],
    properties: {
        industry: "EdTech"
    }
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://api.jetadmin.io" path="/api/projects/:PROJECT_NAME/groups/:GROUP_ID/" method="patch" summary="Update existing project team" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="PROJECT_NAME" type="string" %}
Unique project name (can be taken from Jet Admin project URL)
{% endswagger-parameter %}

{% swagger-parameter in="path" name="GROUP_ID" type="number" %}
Group ID
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
Token authentication, example: 

\




`Authorization: ProjectToken f42a3cab3f146b283701a4e314f1c7ba57fdb59e`
{% endswagger-parameter %}

{% swagger-parameter in="body" name="name" type="string" %}
Group name, example: "Sales"
{% endswagger-parameter %}

{% swagger-parameter in="body" name="super_group" type="boolean" %}
If group will have all permissions
{% endswagger-parameter %}

{% swagger-parameter in="body" name="project_permissions" type="array" %}
Array of permissions
{% endswagger-parameter %}

{% swagger-parameter in="body" name="properties" type="object" %}
JSON Object, example: {"industry": "New York"}
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```javascript
{
    id: 35091
    name: "Sales"
    description: ""
    super_group: false
    project_permissions: [
        {
            id: 525
            permission_type: "model"
            permission_object: "jet_bridge.users_user"
            permission_actions: "r"
            date_add: "2019-03-22T19:03:02.425689+03:00"
        }
    ],
    properties: {
        industry: "EdTech"
    }
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://api.jetadmin.io" path="/api/projects/:PROJECT_NAME/groups/:GROUP_ID/" method="delete" summary="Delete existing project team" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="PROJECT_NAME" type="string" %}
Unique project name (can be taken from Jet Admin project URL)
{% endswagger-parameter %}

{% swagger-parameter in="path" name="GROUP_ID" type="number" %}
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

## For projects with multiple environments

{% swagger baseUrl="https://api.jetadmin.io" path="/api/projects/:PROJECT_NAME/:ENVIRONMENT_NAME/groups/" method="get" summary="Get list of all project teams" %}
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
[
    {
        id: 35091
        name: "Sales"
        description: ""
        super_group: false
        project_permissions: [
            {
                id: 525
                permission_type: "model"
                permission_object: "jet_bridge.users_user"
                permission_actions: "r"
                date_add: "2019-03-22T19:03:02.425689+03:00"
            }
        ],
        properties: {
            industry: "EdTech"
        }
    }
]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://api.jetadmin.io" path="/api/projects/:PROJECT_NAME/:ENVIRONMENT_NAME/groups/" method="post" summary="Create new project team" %}
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

{% swagger-parameter in="body" name="name" type="string" %}
Group name, example: "Sales"
{% endswagger-parameter %}

{% swagger-parameter in="body" name="super_group" type="boolean" %}
If group will have all permissions
{% endswagger-parameter %}

{% swagger-parameter in="body" name="project_permissions" type="array" %}
Array of permissions
{% endswagger-parameter %}

{% swagger-parameter in="body" name="properties" type="object" %}
JSON Object, example: {"industry": "New York"}
{% endswagger-parameter %}

{% swagger-response status="201" description="" %}
```javascript
{
    id: 35091
    name: "Sales"
    description: ""
    super_group: false
    project_permissions: [
        {
            id: 525
            permission_type: "model"
            permission_object: "jet_bridge.users_user"
            permission_actions: "r"
            date_add: "2019-03-22T19:03:02.425689+03:00"
        }
    ],
    properties: {
        industry: "EdTech"
    }
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://api.jetadmin.io" path="/api/projects/:PROJECT_NAME/:ENVIRONMENT_NAME/groups/:GROUP_ID/" method="patch" summary="Update existing project team" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="ENVIRONMENT_NAME" type="string" %}
Environment name in URL
{% endswagger-parameter %}

{% swagger-parameter in="path" name="PROJECT_NAME" type="string" %}
Unique project name (can be taken from Jet Admin project URL)
{% endswagger-parameter %}

{% swagger-parameter in="path" name="GROUP_ID" type="number" %}
Group ID
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
Token authentication, example: 

\




`Authorization: ProjectToken f42a3cab3f146b283701a4e314f1c7ba57fdb59e`
{% endswagger-parameter %}

{% swagger-parameter in="body" name="name" type="string" %}
Group name, example: "Sales"
{% endswagger-parameter %}

{% swagger-parameter in="body" name="super_group" type="boolean" %}
If group will have all permissions
{% endswagger-parameter %}

{% swagger-parameter in="body" name="project_permissions" type="array" %}
Array of permissions
{% endswagger-parameter %}

{% swagger-parameter in="body" name="properties" type="object" %}
JSON Object, example: {"industry": "New York"}
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```javascript
{
    id: 35091
    name: "Sales"
    description: ""
    super_group: false
    project_permissions: [
        {
            id: 525
            permission_type: "model"
            permission_object: "jet_bridge.users_user"
            permission_actions: "r"
            date_add: "2019-03-22T19:03:02.425689+03:00"
        }
    ],
    properties: {
        industry: "EdTech"
    }
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://api.jetadmin.io" path="/api/projects/:PROJECT_NAME/:ENVIRONMENT_NAME/groups/:GROUP_ID/" method="delete" summary="Delete existing project team" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="ENVIRONMENT_NAME" type="string" %}
Environment name in URL
{% endswagger-parameter %}

{% swagger-parameter in="path" name="PROJECT_NAME" type="string" %}
Unique project name (can be taken from Jet Admin project URL)
{% endswagger-parameter %}

{% swagger-parameter in="path" name="GROUP_ID" type="number" %}
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
