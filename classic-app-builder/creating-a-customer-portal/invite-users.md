---
description: >-
  In this section you will learn how to link set Users and Permissions for
  creating a customer portal
---

# Users & Permissions

The key functionality of any Portal is that any user or group of users see and interact **only with their data**. In this step, we'll invite our users and set permissions to turn our Airtable app into a **secure portal**.

### Invite Users

Click `Share` and add the email of a user. Then we can invite this user to the existing team or create a New Team by clicking `Add a new Team`. In our example, we build a portal for corporate clients, so we'll create separate teams for every company we work with.

1. Click on the `Share` button
2. Paste the **Email** you want to send an invite to
3. Click on the `Team` Icon
4. Choose `Add a New` Team
5. Write the **Name** of the **New Team**
6. Click on the `Create` button

{% @arcade/embed flowId="4S1c4rKJWzVxvot6V2Rq" url="https://app.arcade.software/share/4S1c4rKJWzVxvot6V2Rq" %}

{% hint style="info" %}
In Jet Admin, **Teams** are the groups of users with the same permissions
{% endhint %}

Then **send invites** to the users.&#x20;

{% @arcade/embed flowId="WdxQ2HoaddaIOJMPRjKS" url="https://app.arcade.software/share/WdxQ2HoaddaIOJMPRjKS" %}

### Set the Data Separation

**Team Properties** and **User Properties** are used to set the data separation in Jet Admin. For each team or user, we add a `Property` that uniquely identifies a company or a client, such as `domain` or `email`. In our case, we use the company name:

1. Click on the **Add Property**
2. **Choose the Name of the Property**
3. Click on the `Create` button
4. Set the property of the team

{% @arcade/embed flowId="1vVYyB8kUeFeCEFYvDDe" url="https://app.arcade.software/share/1vVYyB8kUeFeCEFYvDDe" %}

{% hint style="info" %}
To be able to separate data, we need to have the property value in our data
{% endhint %}

Next, we need to **filter** our Portal's data by the property. Select the component you want to separate data for, proceed to filters, and set them `Client field` to match `Client property` what we've created.

1. Choose the **Table**
2. Click on the `Filter` icon
3. Choose **Client -> Client equals**
4. Click on the `Formula` icon
5. Choose **Team Properties -> Client**

{% @arcade/embed flowId="xtNGUpI44uaOZz1tBtxl" url="https://app.arcade.software/share/xtNGUpI44uaOZz1tBtxl" %}

### Set Permissions

Additionally, we want our Coffee Beans employees to interact only with the portal page we've created. For this, go to the **Teams** and set page-level permissions to allow access to the `Tasks` , `Tasks-edit` and the `Tasks-create` pages:

![](../../.gitbook/assets/Quickstart-portal19.gif)

Now, let's check how that works: the Beans Coffee employee that we've invited can see **only their company's projects**:

![](../../.gitbook/assets/Quickstart-portal22.gif)
