---
description: How to use Xano API to sign your users into Jet Admin
---

# Xano Auth

{% embed url="https://youtu.be/KY24zB7yn2A" %}
Video version of this guide
{% endembed %}

## Pre-requisites

To successfully integrate this authentication method, you will need a few things:

* **Xano Account**: Ensure you have an active Xano account.
* **JetAdmin Account**: Similarly, a JetAdmin account is required. [Register](https://app.jetadmin.io/projects/create) if you haven't already.
* [**User Table in Xano**](xano-auth.md#xano-users-table): Set up a user table in your Xano project. This table must include fields for email and password.
* [**Auth API Endpoints**](xano-auth.md#xano-authentication-api): Familiarize yourself with creating and managing API endpoints in Xano, as these will be essential for authentication processes.

## Xano users table

Assuming you already have Xano and JetAdmin accounts, your Xano users table should have at least the "email" and "password" columns.

Ensure the "password" column has a "password" type.

## Xano authentication API

You will be using two endpoints:

* **auth/login** to login the user and get the authentication token
* **auth/me** to get the records belonging to the token

Check whether you have those endpoints created. And if you don't, create them.

Please refer to [Xano documentation](https://docs.xano.com/api/the-basics/authenticated-request) if you have any trouble setting it up.

{% @arcade/embed flowId="pRXByxmjUv1YkMuBtAWE" url="https://app.arcade.software/share/pRXByxmjUv1YkMuBtAWE" %}

## Setting up custom authentication

### 1. Creating a new resource for queries

While in JetAdmin, create a separate resource to host the Base URL.

1. While in the builder, head over to the "Data" tab on your left panel
2. Click on "Add Resource"
3. Select the "Rest API"
4. Name your resource
5. Head over to Xano and copy the base URL
6. Paste the Base URL and save

{% @arcade/embed flowId="3K6KTIimCqIYciyTEAZw" url="https://app.arcade.software/share/3K6KTIimCqIYciyTEAZw" %}

### 2. Creating a new custom authentication method

You will need to create a new custom authentication method.

1. While in the builder, head over to "Sign In & Sign Up" settings
2. Go to "Authentication" settings
3. Add a new external authentication method and select "Custom authentication"
4. Define the name, icon, and the team that the users will be assigned to
5. Head over to login workflow creation

{% @arcade/embed flowId="lrtOEuqEiXRHOFKgAKVS" url="https://app.arcade.software/share/lrtOEuqEiXRHOFKgAKVS" %}

### 3. Configuring login workflow

#### 3.1 Creating a node for _auth/login_ request

Firstly, you need to create a new workflow node that would call the "auth/login" endpoint and pass the "email" and "password" inputs as query parameters.

1. Create a new node and select the "Xano auth" resource
2. Create a new HTTP request
3. Set it to "POST" and fill in the endpoint URL (.../auth/login)
4. Create "email" and "password" query params to be sent to Xano
5. Create "email" and "password" inputs to get them from Jet Admin
6. Pass the values from inputs to query params
7. Fill in the test values and test the request

{% @arcade/embed flowId="3m8dkBfU0ZfyunQzLXJM" url="https://app.arcade.software/share/3m8dkBfU0ZfyunQzLXJM" %}

#### 3.2 Creating a node for the _auth/me_ request

1. Create a new node and select the "Xano auth" resource
2. Create a new HTTP request
3. Set it to "GET" and fill in the endpoint URL (.../auth/me)
4. Create an "Authorization" header to be sent to Xano
5. Create "authToken" input to get them from Jet Admin
6. Pass the token from inputs to query headers (input "Bearer" with a spacebar before the token)
7. Fill in the test value and test the request

{% @arcade/embed flowId="SPnxl42mkeS2kG0eURPI" url="https://app.arcade.software/share/SPnxl42mkeS2kG0eURPI" %}

#### 3.3 Linking inputs and outputs of the workflow

1. Fill in test values for workflow parameters
2. Link "email" and "password" workflow parameters as inputs in the "auth/login" node
3. Link the "authToken" workflow parameter as an input in the "auth/me" node
4. Link workflow parameters from the previous step as workflow output
5. Test and save the workflow

{% @arcade/embed flowId="CAKCHyB2lcaC7AhI8Tch" url="https://app.arcade.software/share/CAKCHyB2lcaC7AhI8Tch" %}

### 4. Changing the sign-up page appearance

1. Publish your changes if you haven't already
2. Disable/enable those methods that you are planning to use
3. Check whether the preview is displaying everything correctly
4. Customize names and icons for your external auth methods

{% @arcade/embed flowId="wVFfkUNydXri2ePP5Qnh" url="https://app.arcade.software/share/wVFfkUNydXri2ePP5Qnh" %}

## Testing the sign-in flow

1. Open up a separate browser instance
2. Navigate to the sign-in page and try to log in using test credentials
3. Check whether you are signed and have appropriate access
4. Get back to your admin panel and check whether the user was created in JetAdmin

{% @arcade/embed flowId="yoGH2Fxaje06HJG45AwH" url="https://app.arcade.software/share/yoGH2Fxaje06HJG45AwH" %}
