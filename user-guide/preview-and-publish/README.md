# ▶ Preview & Publish

## Builder/User/Preview modes

There are three operational modes in Jet Admin: the **Builder mode**, **** the **User mode**, and the **Preview mode.**

## **Builder Mode**

**Builder mode** is where people who are building an app can add data sources, drag-and-drop UI components, customize them, bind them to your data, manage environments, and perform all the necessary work to get your app ready.&#x20;

{% hint style="info" %}
After creating an account, you'll automatically get into the Builder mode with the Administrator permissions.
{% endhint %}

![](../../.gitbook/assets/mcgnvyn.JPG)

## **User Mode**

**User mode**, on the other hand, allows end-users to perform their daily operations in the app. For that, all the changes that have been made in the app have to be published, generating a new page with a new `.../app/...` URL. In this mode, users don't have access to any customization features but can interact with the data according to their permissions.

![](../../.gitbook/assets/fmxyju.JPG)

## **Preview Mode**

**Preview mode** is designed for the builders to quickly preview the app in a user-mode without having to publish an app.

Within the preview mode, a user can:

* **Review** the changes before publishing
* **Discard** changes (will revert back to the last published version)
* **Publish** an app
* **Impersonate** a specific user

![](../../.gitbook/assets/tdjsyu.png)

### Reviewing changes

By clicking on the **"N changes"** label, drill down into the changes history. Here you can view the logs **(2)** and granularly discard changes for broader categories **(1)** or for individual collections, resources, settings, etc. **(3)**

![](../../.gitbook/assets/xncffy.png)

### Impersonating users

When building an app, it's usually difficult to get the right idea of how page permissions, dynamic filters, or conditional visibility that's been configured will transform into the end-user experience.&#x20;

The impersonation feature allows you to quickly **preview** an app **through the eyes** of a particular user. In the example case below, we've denied access for Michael to the `Customers` page and set the user to see only records where `Customer ID = 1` the `Orders` table.

![](<../../.gitbook/assets/ftjgyu (1).gif>)

To start previewing as a particular user, just click on the "Previewing as" button, and choose a user to impersonate

![](../../.gitbook/assets/dnctfv.png)
