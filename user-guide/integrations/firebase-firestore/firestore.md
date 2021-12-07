# Firestore

Connect Jet Admin to Firebase's Admin API to create custom internal tools to manage your Firebase application.

Once Firebase is added to Jet Admin, you'll be able to manage your users, query and update Firebase Real-time Databases as well as query Firestore.

### 1. Get Firebase Key

To get Firebase Key you need to add Firebase to your Google project. First, go to [Firebase ](https://firebase.google.com)and just click **Get Started**.

![](<../../../.gitbook/assets/image (564).png>)

Choose your Google Account to start. **** Then you need to click on Add project to get Firebase Key.

![](<../../../.gitbook/assets/GIF (119).gif>)

Then you need to go to the Service Accounts to generate a new private key. Once you have generated a private key, it will automatically download to your computer.

![](<../../../.gitbook/assets/GIF (120).gif>)

### 2. Add Firebase to Jet Admin

Add a new resource to an existing project or connect to Firebase when creating a new project. The integration process will be the same in both cases.

![](<../../../.gitbook/assets/image (816).png>)

Select Firebase from the list of available resources and enter your private key in JSON format. You can upload JSON file or copy the code to Service Token field.

![](<../../../.gitbook/assets/image (825).png>)

An example of JSON Service Key obtained from Firebase.

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
