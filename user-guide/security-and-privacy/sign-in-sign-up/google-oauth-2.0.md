---
description: Step-by-step guide to authentication with Google OAuth 2.0
---

# Google SSO OAuth 2.0

If you want to use Google services such as Google Sheets, Google Drive, Google Cloud and many others, this step-by-step guide can help you with **Google OAuth 2.0** authentication.

Once you have created the project and selected the Rest API resource, you also selected the [OAuth 2.0](../../integrations/rest-api/oauth-2.0.md) authentication method - you need to select a provider.

## Google Developers Console

### 1. Google API Console

Visit the [Google API Console](https://console.developers.google.com/) to obtain OAuth 2.0 credentials such as a `Client ID` and `Client secret` that are known to both Google and Jet Admin.

### 2. Create a new project

![](<../../../.gitbook/assets/image (412).png>)

### 3. Specify new project details

Specify `Project name` and `Location` then click the **Create** button.

![](<../../../.gitbook/assets/image (414).png>)

### 4. Enable APIs and Services

In the control panel, enable the API and Services you plan to use.&#x20;

![](<../../../.gitbook/assets/image (415).png>)

The API library looks like this. You can choose any service you are plan to use, but we will go through the Google Sheet API.

![](<../../../.gitbook/assets/image (428).png>)

Once you have selected the API and services, click the **Enable** button.

![](<../../../.gitbook/assets/image (416).png>)

### 5. Create Credentials&#x20;

To use this API, you need credentials. Go to the credentials menu to get started.

![](<../../../.gitbook/assets/image (418).png>)

Сonfigure the OAuth consent screen:

![](<../../../.gitbook/assets/image (419).png>)

Choose how you want to configure and register your app, including your target users. You can only associate one app with your project. Then click **Create**.

![](<../../../.gitbook/assets/image (420).png>)

Specify the application name, scroll down the page, and click **Save**.

![](<../../../.gitbook/assets/image (421).png>)

Go to the credentials menu and click **Create credentials**. Then select OAuth Client ID.

![](<../../../.gitbook/assets/image (423).png>)

Then you need to select the application type. In the drop-down list, select Web application. Specify name, you also can add OAuth Redirect URL, then click **Create**.\
`https://api-dev.jetadmin.io/api/create_oauth_token_complete/`

![](<../../../.gitbook/assets/GIF (2).gif>)

Congratulations, your client ID and client secret created.

![](<../../../.gitbook/assets/image (425).png>)

### 5. Adding resource

To complete the process of adding a resource, we need to fill in the scopes field.

![](<../../../.gitbook/assets/image (426).png>)

You can find the necessary information [here](https://developers.google.com/identity/protocols/oauth2/scopes#sheets). For our case, the scopes look like this.

| Scopes                                                | Description                                                     |
| ----------------------------------------------------- | --------------------------------------------------------------- |
| https://www.googleapis.com/auth/spreadsheets          | See, edit, create, and delete your spreadsheets in Google Drive |
| https://www.googleapis.com/auth/spreadsheets.readonly | View your Google Spreadsheets                                   |

### Conclusion&#x20;

Congratulations! Now you are ready to authenticate with Google OAuth 2.0. If you still have any questions, please contact us for help.
