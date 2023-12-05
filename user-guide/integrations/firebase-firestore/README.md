---
description: How to build business apps on top of Firebase data
---

# Firebase / Firestore

In this article, we'll review the integration with Firebase and will go through the steps necessary to connect it to Jet Admin

### Connecting Firebase

To connect to Firebase from the new app flow, follow the steps:

1. Select the `Data` Tab from the **left menu bar**
2. Click on the `Add Resource` button
3. Choose **Firebase** resource

{% @arcade/embed flowId="02StOgDDTvaChE64xFrW" url="https://app.arcade.software/share/02StOgDDTvaChE64xFrW" %}

### Obtain service token

You'll need to paste a service token to allow your Firebase to interact with Jet. You can copy and paste or upload a JSON snippet as a file.

To copy and paste a JSON snippet, follow the steps:

1. In the form, paste the **Service Token**
2. Alternatively, you can upload the Service token as a file

{% @arcade/embed flowId="niLLzEwkvhIKSCNtaAXw" url="https://app.arcade.software/share/niLLzEwkvhIKSCNtaAXw" %}

{% hint style="danger" %}
**It's critical** to have a **proper data structure** in your Firebase database. Otherwise, Jet might not detect all or some parts of it. Read the official Firebase article properly to learn how to structure your data.
{% endhint %}

To obtain a service key, follow the steps:

1. Click on the `Settings` button
2. Choose **Project Settings**
3. Go to the **Service Account tab**
4. Click on the `Generate new private key` button
5. Click on the `Generate key` button

{% @arcade/embed flowId="HgPGN726gSBgt5035iCh" url="https://app.arcade.software/share/HgPGN726gSBgt5035iCh" %}

Then you'll need to select the database type: Firestore or Realtime DB:

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
To learn more about Firestore and Realtime DB, check the [**official Firebase article**](https://firebase.google.com/docs/database/rtdb-vs-firestore)**.**
{% endhint %}

Further steps vary based on the type of database you want to connect to: Firestore or Realtime DB.
