# Airtable

In this article, we'll review the integration with Airtable, and its characteristics and will go through the steps necessary to connect it to Jet Admin

{% embed url="https://www.youtube.com/watch?v=HOiRAbCOcss&list=PLSkzi9eq0vBnUGMnwXrRRVo9TXUjZ7uSj&index=19&ab_channel=JetAdmin" %}

###

{% hint style="info" %}
**API keys are deprecated by the end of January 2024.**

Airtable's API keys stopped working and you will have to migrate to **personal access tokens**. However, you don't need a **Personal access tokens** to connect Airtable to Jetadmin. Just logging in with Airtable when creating a new resource is enough
{% endhint %}

### Connect Airtable to Jetadmin

1. On Jetadmin's builder side, click 'Add Resource' from the data section on the left-side menu
2. Choose Airtable
3. Click on 'Sign In to Airtable' button
4. Click on 'Add a base'
5. Choose the needed base or workspace
6. Click 'Grant access'
7. Choose the base needed
8. Click the 'Choose tables' button
9. Select/unselect the needed tables and choose a **view** for each table
10. Click the 'Add Resource' button.

{% @arcade/embed url="https://app.arcade.software/share/hsHDJdkTBCT823AUWCtD" flowId="hsHDJdkTBCT823AUWCtD" %}

### Choosing connection mode

After that, you need to choose how you'd like your Airtable to be integrated with Jet Admin. You can either connect directly or **sync it** with Jet's internal database to get extended functionality.

If you want to be able to **combine your Airtable data** with data from other data sources, such as Firebase, Google Sheets, or even REST API within the same tables, you should choose the **"Sync" connection** for Airtable. You can learn more about it here:

![](https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2F4fnMpNeuHFN02dswTz5X%2Filhj.JPG?alt=media\&token=c2122ca0-2b81-407c-8b43-437f62c5422f)

After having connected your Airtable, you'll be prompted to choose pages you want Jet Admin to generate **an admin panel (CRUD pages)** for.

### Airtable Views

On Airtable side, you can create different views for each table. Each view allows you to filter and sort records. In Jetadmin you can choose to use only one view for each table when creating the resource. To view all records in each table, choose the main view 'All'.

The image below will show you the differences between the main view and the filtered views:

<figure><img src="https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2F850UoM3lHRZCpUY59GJ3%2Fimage.png?alt=media&#x26;token=670c5812-41f7-4a82-9953-49d131cc6847" alt=""><figcaption></figcaption></figure>

### Switch Airtable's Views

To switch to other views for each table, follow the steps below:

1. Click 'Edit resource' from the resource's settings menu
2. Click on 'Choose tables'
3. Select the needed views for each table
4. Click 'Update resource'.

<figure><img src="https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2FMacRjNlTGxUcSiihlsWy%2Fimage.png?alt=media&#x26;token=6102923d-70ed-43c6-a100-ac6ed914253f" alt=""><figcaption></figcaption></figure>

{% content-ref url="../../synced-tables/" %}
[synced-tables](../../synced-tables/)
{% endcontent-ref %}
