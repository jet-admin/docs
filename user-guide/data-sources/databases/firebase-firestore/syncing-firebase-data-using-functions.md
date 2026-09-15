---
description: >-
  This is a more efficient data syncing method with Firebase. This replaces the
  outdated snapshot-based approach, eliminating the need to update entire
  collections for small changes.
---

# Syncing Firebase Data Using Functions

{% hint style="info" %}
The "Using Functions" feature is exclusive to **Firebase Blaze plan** users.
{% endhint %}

### Step-by-Step Guide <a href="#step-by-step-guide" id="step-by-step-guide"></a>

#### **Scenario 1: Firebase Data Source Already Connected** <a href="#scenario-1-firebase-data-source-already-connected" id="scenario-1-firebase-data-source-already-connected"></a>

1. Navigate to **Data > Connected Data Sources**.
2. Locate your Firebase data source and click on the **three dots** next to its name in top menu.
3. Select **Stop Sync**. (This action does not affect your data.)
4. Choose **Use Direct Connection**.
5. Click on the **three dots** again and select **Sync to Jet Tables**.
6. When prompted, choose the **"Using Functions"** option.
7. Follow the instructions to meet the required permissions:
   * Assign **Service Usage Admin**, **Service Account User**, and **Cloud Functions Admin** roles to the respective principals.
8. Click **Check Configuration**. The remaining steps will complete automatically.

{% @arcade/embed flowId="7lSutjZkYBXh130RbXOK" url="https://app.arcade.software/share/7lSutjZkYBXh130RbXOK" %}

#### **Scenario 2: Firebase Data Source Not Already Connected** <a href="#scenario-2-firebase-data-source-not-already-connected" id="scenario-2-firebase-data-source-not-already-connected"></a>

1. Add a new Firebase resource in Jet Admin following the instructions [here](https://docs.jetadmin.io/videos/connecting-data-sources/getting-started-with-firebase).
2. When prompted, choose the **"Using Functions"** option.
3. Follow the instructions to meet the required permissions:
   * Assign **Service Usage Admin**, **Service Account User**, and **Cloud Functions Admin** roles to the respective principals.
4. Click **Check Configuration**. The remaining steps will complete automatically.

### Why Use "Using Functions"?

{% hint style="info" %}
The "Using Functions" method provides significant advantages e.g. efficiency Only updates the changed document, saving bandwidth and processing time.
{% endhint %}

