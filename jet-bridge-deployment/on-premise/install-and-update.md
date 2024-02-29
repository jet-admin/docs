# Install & Update

## Requirements

* Command-line experience
* Docker installed
* License key (contact our sales)

{% hint style="info" %}
Access to **gitlab.com/jet-admin/jet-onpremise** is necessary before installing.&#x20;
{% endhint %}

## [Get started with on-premise](https://app.jetadmin.io/projects?builder\_link=project/on-premise)

## Installation

#### 1. Download on-premise **package**

You should have access to [gitlab.com:jet-admin/jet-onpremise](https://gitlab.com/jet-admin/jet-onpremise) repository. We grant you access to the repository by your **USERNAME** and give you **Access Token**.&#x20;

Change **USERNAME** to your [gitlab.com](https://gitlab.com/) username. Running the following command will ask you to enter password which you should fill with your **Access Token** value.

```
git clone https://USERNAME@gitlab.com/jet-admin/jet-onpremise.git && cd jet-onpremise
```

#### 2. Create **Initial config** file and set **Required parameters**

```
./scripts/generate_config/run.sh
```

After running this command you should have **.env** file created in the current directory. You should set the following required parameters inside it.

```
#------------------------------------------------------------------------------
# (*) Required parameters
#------------------------------------------------------------------------------

# - License Key

LICENSE_KEY=

# - General

BUILD_NAME=master
NGINX_PORT=80
CENTRIFUGO_PORT=8000

COMMON_SECRET_KEY=
COMMON_DEBUG=0
COMMON_FRONTEND_URL=http://localhost
COMMON_FRONTEND_HOST=localhost
COMMON_BACKEND_URL=http://api.localhost
COMMON_BACKEND_HOST=api.localhost
COMMON_JET_BRIDGE_CLOUD_URL=http://jetbridge.localhost/api/
COMMON_JET_BRIDGE_CLOUD_HOST=jetbridge.localhost
COMMON_CENTRIFUGO_URL=ws://localhost:8000/connection/websocket
```

#### 3. Login to images repository using credentials with access to **Jet Admin On-premise**

Use your login & password on **gitlab.com**.

```
docker login registry.gitlab.com
```

#### 4. Download latest version (Start from this step in case of update)

```
docker-compose pull
```

#### 5. Run **Jet Admin** application (can take up to 30 seconds)

It should run all **Jet Admin** components in background and start application at NGINX\_PORT (80 by default).

```
docker-compose up -d
```

#### 6. Confirm that all containers are running

```
docker-compose ps
```

**Done!** Navigate to your server's IP address in a web browser

## Updating

#### 1. Go to the previously installed on-premise package directory

```
cd jet-onpremise
```

#### 2. Update target version if needed

Open **.env** file in the current directory

```
BUILD_NAME=2.4.3
```

#### 3. Download latest version

```
docker-compose pull
```

#### 4. Restart **Jet Admin** application (can take up to 30 seconds)

It should restart all **Jet Admin** components and run them in background.

```
docker-compose up -d
```
