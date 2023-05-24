# Configuration

## Setting up your configuration

You can specify **Jet Bridge** configuration through one of the following methods:\
command-line arguments, config file, or environment variables. Here are examples:

### Method 1. Command-line arguments

{% hint style="info" %}
Warning: arguments name should be lowercase. Other methods are case insensitive
{% endhint %}

```bash
jet_bridge --database_engine=postgresql \
    --database_host=localhost \
    --database_port=5432 \
    --database_user=user \
    --database_password=password \
    --database_name=mydb
```

### Method 2. Config file

{% code title="jet.ini" %}
```
[JET]
DATABASE_ENGINE=postgresql
DATABASE_HOST=localhost
DATABASE_PORT=5432
DATABASE_NAME=mydb
DATABASE_USER=user
DATABASE_PASSWORD=password
```
{% endcode %}

### Method 3. Environment variables

```bash
DATABASE_ENGINE=postgresql \
    DATABASE_HOST=localhost \
    DATABASE_PORT=5432 \
    DATABASE_NAME=mydb \
    DATABASE_USER=user \
    DATABASE_PASSWORD=password \
    jet_bridge
```

### Method 4. settings.py (Django package)

```python
# For Django package database settings are taken from 
# DATABASES['default'] setting so you don't need to specify it.
JET_JWT_VERIFY_KEY='YOUR_CUSTOM_JWT_VERIFY_KEY'
```

## All available settings

### Required settings

| **Name**               | Description                                                                                            |
| ---------------------- | ------------------------------------------------------------------------------------------------------ |
| **DATABASE\_ENGINE**   | <p>Database engine, one of: <br>postgresql<br>mysql<br>oracle<br>mssql+pyodbc<br>sqlite</p><p>none</p> |
| **DATABASE\_HOST**     | Database host                                                                                          |
| **DATABASE\_PORT**     | Database port                                                                                          |
| **DATABASE\_USER**     | Database user                                                                                          |
| **DATABASE\_PASSWORD** | Database password                                                                                      |
| **DATABASE\_NAME**     | Database name or path (SQLite)                                                                         |

### Optional settings

| Name                            | Default                                                                                                  | Description                                                                                   |
| ------------------------------- | -------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| **ADDRESS** (optional)          | 0.0.0.0                                                                                                  | Jet Bridge address                                                                            |
| **PORT** (optional)             | 8888                                                                                                     | Jet Bridge port                                                                               |
| **SSL\_CERT** (optional)        | -- none --                                                                                               | File path to SSL certificate                                                                  |
| **SSL\_KEY** (optional)         | -- none --                                                                                               | File path to SSL private key                                                                  |
| **CONFIG** (optional)           | /etc/jet.conf                                                                                            | Path to config file                                                                           |
| **DEBUG** (optional)            | false                                                                                                    | Run in debug mode                                                                             |
| **READ\_ONLY** (optional)       | false                                                                                                    | Data read only                                                                                |
| **BASE\_URL** (optional)        | https://example.com/                                                                                     | Jet Bridge base URL                                                                           |
| **WEB\_BASE\_URL** (optional)   | [https://app.jetadmin.io](https://app.jetadmin.io)                                                       | Jet Admin frontend application base URL                                                       |
| **API\_BASE\_URL** (optional)   | [https://api.jetadmin.io/api](https://api.jetadmin.io/api)                                               | Jet Admin API base URL                                                                        |
| **MEDIA\_STORAGE** (optional)   | default                                                                                                  | Media storage type                                                                            |
| **MEDIA\_ROOT** (optional)      | media                                                                                                    | Media root                                                                                    |
| **MEDIA\_BASE\_URL** (optional) | -- none --                                                                                               | Media base URL                                                                                |
| **COOKIE\_SAMESITE** (optional) | None                                                                                                     | Cookie Samesite attribute                                                                     |
| **COOKIE\_SECURE** (optional)   | true                                                                                                     | Is host with HTTPS                                                                            |
| **COOKIE\_DOMAIN** (optional)   | -- none --                                                                                               | Cookie domain                                                                                 |
| **COOKIE\_COMPRESS** (optional) | false                                                                                                    | GZIP cookies that may be large in size                                                        |
| **THREADS** (optional)          | number of CPUs                                                                                           | Number of threads Jet Bridge will create to serve requests                                    |
| **CORS\_HEADERS** (optional)    | true                                                                                                     | Specifies if Jet Bridge should automatically add CORS headers or want to add them on your own |
| **JWT\_VERIFY\_KEY** (optional) | See [Validate JWT Token](../../user-guide/integrations/rest-api/jet-requests-auth.md#validate-jwt-token) | JWT public key to verify user requests                                                        |

