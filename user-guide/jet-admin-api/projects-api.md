# Projects API

{% swagger method="get" path="/api/projects/:PROJECT_NAME/" baseUrl="https://api.jetadmin.io" summary="Get project information" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="PROJECT_NAME" required="true" %}
Unique project name (can be taken from Jet Admin project URL)
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" required="true" %}
Token authentication, example: 

\




`Authorization: Bearer f42a3cab3f146b283701a4e314f1c7ba57fdb59e`
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
  "owner": {
    "username": "f1nal@cgaming.org",
    "first_name": "Denis",
    "last_name": "Kildishev",
    "email": "f1nal@cgaming.org",
    "photo": "https://api-dev.jetadmin.io/media/user/photo/2020/05/26/1628232.jpeg",
    "uid": "1025c221-948a-4b7c-a58b-fa7cf816a72c",
    "is_staff": true,
    "email_verified": true
  },
  "is_owner": true,
  "unique_name": "test_1064",
  "name": "test",
  "api_base_url": "",
  "messages_url": "",
  "color": "blue",
  "default_theme": null,
  "logo": null,
  "url": "",
  "domain": null,
  "default_group": null,
  "user": {
    "uid": "fea0112e-55c5-4b58-b49a-209e6d61322f",
    "properties": {
    },
    "date_add": "2021-11-23T11:48:33.350791+03:00"
  },
  "group": {
    "id": "b81051a4-9bfb-459f-98bb-96d4fdd263a5",
    "uid": "b81051a4-9bfb-459f-98bb-96d4fdd263a5",
    "environment": "prod",
    "name": "Administrator",
    "description": "",
    "permissions_group": "full_access",
    "super_group": true,
    "project_permissions": [
    ],
    "properties": {
    },
    "protected": true,
    "params": {
    }
  },
  "demo": false,
  "parent": null,
  "jobs": [
  ],
  "tokens": [
  ],
  "company": false,
  "resources": [
    {
      "environment": "prod",
      "unique_name": "31a5523e-600d-4308-8f50-4bb72db2d34c",
      "name": "Google Sheets",
      "type": "rest_api",
      "type_item": "googlesheets",
      "deploy": "",
      "media_url_template": "",
      "token": null,
      "params": {
        "files": [
          {
            "uid": "0f5b9089-ab23-49c1-a7bf-b2928a3db94f",
            "file": {
              "id": "1Dr17_aFFFTY7pavcIn2Qf_2ezJ_lSjRIBgUFFmB5d5k",
              "kind": "drive#file",
              "name": "jet_admin_test",
              "mimeType": "application/vnd.google-apps.spreadsheet",
              "capabilities": {
                "canEdit": true,
                "canDelete": true
              }
            },
            "range": "A:J",
            "sheet": {
              "name": "tt",
              "index": 0
            }
          }
        ],
        "featured": false,
        "base_http_query": {
          "body": "",
          "method": "GET",
          "headers": [
          ],
          "body_type": "JSON",
          "auth_params": {
          },
          "query_params": [
          ],
          "response_type": "json",
          "request_tokens": {
          }
        }
      },
      "secret_tokens": [
        {
          "name": "oauth_access_token",
          "type": "oauth",
          "draft": false,
          "deleted": false
        }
      ],
      "storages": [
      ],
      "draft": false,
      "deleted": false
    }
  ],
  "default_environment": {
    "unique_name": "prod",
    "name": "Production",
    "color": "green",
    "params": {
    },
    "user": {
      "uid": "fea0112e-55c5-4b58-b49a-209e6d61322f",
      "properties": {
      },
      "date_add": "2021-11-23T11:48:33.350791+03:00"
    },
    "group": {
      "id": "b81051a4-9bfb-459f-98bb-96d4fdd263a5",
      "uid": "b81051a4-9bfb-459f-98bb-96d4fdd263a5",
      "environment": "prod",
      "name": "Administrator",
      "description": "",
      "permissions_group": "full_access",
      "super_group": true,
      "project_permissions": [
      ],
      "properties": {
      },
      "protected": true,
      "params": {
      }
    },
    "date_add": "2021-11-23T11:48:33.331202+03:00"
  },
  "environments": [
    {
      "unique_name": "prod",
      "name": "Production",
      "color": "green",
      "params": {
      },
      "user": {
        "uid": "fea0112e-55c5-4b58-b49a-209e6d61322f",
        "properties": {
        },
        "date_add": "2021-11-23T11:48:33.350791+03:00"
      },
      "group": {
        "id": "b81051a4-9bfb-459f-98bb-96d4fdd263a5",
        "uid": "b81051a4-9bfb-459f-98bb-96d4fdd263a5",
        "environment": "prod",
        "name": "Administrator",
        "description": "",
        "permissions_group": "full_access",
        "super_group": true,
        "project_permissions": [
        ],
        "properties": {
        },
        "protected": true,
        "params": {
        }
      },
      "date_add": "2021-11-23T11:48:33.331202+03:00"
    }
  ],
  "features": {
    "users": {
      "enabled": true,
      "params": {
        "max_users": null
      }
    },
    "environments": {
      "enabled": true
    },
    "tasks": {
      "enabled": true
    },
    "domain": {
      "enabled": true
    },
    "white_label": {
      "enabled": true
    },
    "custom_views": {
      "enabled": true
    },
    "sso": {
      "enabled": false
    },
    "activity_log": {
      "enabled": true
    },
    "groups": {
      "enabled": true
    },
    "3rd_party_resources": {
      "enabled": true
    },
    "custom_resources": {
      "enabled": true
    },
    "customer_sign_up": {
      "enabled": false
    }
  },
  "subscription": {
    "plan": {
      "unique_name": "internal_tools_pro",
      "name": "Internal Tools Pro",
      "subtitle": "",
      "description": "",
      "price": "1.00",
      "activities_per_price": null,
      "activities_max": null,
      "purchasable": true,
      "ordering": 3
    },
    "billing_period": "month",
    "date_begin": "2021-11-23T11:48:33.322669+03:00",
    "date_end": "2021-12-07T11:48:33.322669+03:00",
    "periods": [
    ],
    "params": {
      "free_trial": {
        "days": 14
      }
    },
    "is_active": true
  },
  "params": {
    "layout": "double_menu_left",
    "activity_log_enabled": true,
    "collaboration_enabled": true
  }
}

```
{% endswagger-response %}
{% endswagger %}
