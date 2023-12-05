---
description: In this section you will learn how to use Firebase Cloud Storage
---

# Firebase Cloud Storage

Before you can use Firebase Cloud storage, you need to obtain a service token key. Follow the steps below to integrate Firebase storage with Jet.‌

### Get Firebase Storage JSON Key <a href="#1-get-firebase-key" id="1-get-firebase-key"></a>

To get the JSON key you need to add Firebase to your Google project. First, go to [Firebase](https://firebase.google.com/) and just click **Get Started**.

![](<../../../.gitbook/assets/image (791).png>)

To create a project, follow the steps:

1. Click on the `Add Project` button
2. Choose a name for the project
3. Click on the `Continue` button
4. Select the **Google Account**
5. Click on the `Create Project` button

{% @arcade/embed flowId="lQDBBnBzvaYovj6DJgYW" url="https://app.arcade.software/share/lQDBBnBzvaYovj6DJgYW" %}

Then go to the Service Accounts to generate a new JSON private key. Once you generate a private key, it will automatically download to your computer.​

To generate a private key, follow the steps:

1. Click on the `Settings` of the **Project Overview**
2. Click on the `Project Settings`
3. Go to the **Service Accounts** tab
4. Click on the `Generate new private key` button

{% @arcade/embed flowId="Khzwc6u4GUHfVszt1b7m" url="https://app.arcade.software/share/Khzwc6u4GUHfVszt1b7m" %}

### Add Firebase Storage to Jet Admin <a href="#2-add-firebase-to-jet-admin" id="2-add-firebase-to-jet-admin"></a>

Select Firebase Storage from the list of available storage options, upload the JSON file or paste the service token generated for your service account.

![](<../../../.gitbook/assets/image (793).png>)

Here's an example of a JSON Service Key obtained from Firebase:

```javascript
{
  "type": "service_account",
  "project_id": "{your_project_name}",
  "private_key_id": "{your_private_key_id}",
  "private_key": "-----BEGIN PRIVATE KEY-----\{your_private_key}\n-----END PRIVATE KEY-----\n",
  "client_email": "{you_client_email}",
  "client_id": "{your_client_id}",
  "auth_uri": "https://accounts.google.com/o/oauth2/auth",
  "token_uri": "https://oauth2.googleapis.com/token",
  "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
  "client_x509_cert_url": "{you_client_url}"
}
```

Once you have integrated Firebase Storage with Jet you will see a **Storage File Viewer** that'll allow you to access your data. For more information about using storage and uploading files, [see the File Storage and Uploading section.](https://docs.jetadmin.io/user-guide/data/file-storage-and-uploading)

![](../../../.gitbook/assets/GIF213.gif)
