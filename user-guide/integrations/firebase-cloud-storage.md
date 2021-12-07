# Firebase Cloud Storage

Before you can use Firebase Cloud storage, you need to obtain a service token key. Follow the steps below to integrate Firebase storage with Jet.‌

### Get Firebase Storage JSON Key <a href="#1-get-firebase-key" id="1-get-firebase-key"></a>

To get the JSON key you need to add Firebase to your Google project. First, go to [Firebase](https://firebase.google.com) and just click **Get Started**.

![](<../../.gitbook/assets/image (791).png>)

First, Choose your Google Account. Then you need to click on **Add project** to get a Firebase Key.​

![](<../../.gitbook/assets/GIF (316).gif>)

Then you need to go to the Service Accounts to generate a new JSON private key. Once you have generated a private key, it will be automatically downloaded to your computer.​

![](<../../.gitbook/assets/GIF (1) (1).gif>)

### Add Firebase Storage to Jet Admin <a href="#2-add-firebase-to-jet-admin" id="2-add-firebase-to-jet-admin"></a>

Select Firebase Storage from the list of available storage options, upload the JSON file or paste the service token generated for your service account.

![](<../../.gitbook/assets/image (793).png>)

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

Once you have integrated Firebase Storage with Jet you will see a **Storage File Viewer** that'll allow you to access your data.

![](../../.gitbook/assets/GIF213.gif)
