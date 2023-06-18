---
description: Learn how to version apps or revert changes to a previous state.
---

# 🎚 Version Control

Version control allows you to version the applications you build and revert to a previous version if something broke or isn't functioning as intended.

By default, any changes made to a Jet app are automatically saved to the current working version and are immediately visible to all users. However, it is possible to enable app versioning or revert back to a previous state if necessary.

Releases enable users to implement app versioning and release changes using a unique version number that represents the app's specific state. When a release is published, it becomes the live version for users to interact with, providing a secure way to test and deploy changes without causing any disruptions.&#x20;

Jet keeps a detailed record of all modifications made, allowing users to browse through the list of versions and revert the app to a previous state if necessary.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>



### Creating a backup version

{% hint style="info" %}
At the moment, Jet doesn't have an automated backup system so you should save and store relevant versions manually
{% endhint %}

To save a stable version, open your app in the builder mode and click on the "App" icon in the top left corner

<figure><img src="../.gitbook/assets/Group 756 (1).png" alt=""><figcaption></figcaption></figure>

Then choose the environment you want to save the version from (click the gear icon to drill down)

<figure><img src="../.gitbook/assets/Group 755.png" alt=""><figcaption></figcaption></figure>

After that, you can **download the current configuration** and store it in your local storage



<figure><img src="../.gitbook/assets/Group 7571.png" alt=""><figcaption></figcaption></figure>

### Restoring a previous version

To rollback to the previously saved version, you'll need to click upload and select the backup file that's been saved. After that, the changes will be pushed automatically



<figure><img src="../.gitbook/assets/Group 7581.png" alt=""><figcaption></figcaption></figure>
