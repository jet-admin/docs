---
description: In this section you will learn how to create a Custom Component
---

# Create a JavaScript Component

In this tutorial, we'll show you how to create a sample **Custom Сomponent** that you can, later on, extend to satisfy whatever needs you have.

#### 1. Create your JavaScript component project (playground) or clone an example

A JavaScript Component uses [Web Component](https://www.webcomponents.org/introduction) specification to integrate any **JS-based** component to **Jet Admin** – this allows you to use any **Frameworks** and **Libraries** you like as long as you create them as custom **Web Components**. So it can be **React**, **Angular**, or **Vue. js-based** components, or any other.

First, you need to create a **JavaScript Component** project where you can develop and test it. This project will be your playground for creating **JavaScript Components**. It will work the same way as on **Jet Admin** but will make your development easier so that you can use your favorite **IDE** and environment. To make it simpler, you can use some of our ready-to-use starter projects on **GitHub** or use them as a reference:

* React – [https://github.com/jet-admin/jet-flex-view-react-example](https://github.com/jet-admin/jet-flex-view-react-example)
* Angular – [https://github.com/jet-admin/jet-flex-view-angular-example](https://github.com/jet-admin/jet-flex-view-angular-example)

For example, here's an example of cloning React and preparing it for work:

```bash
git clone git@github.com:jet-admin/jet-flex-view-react-example.git
cd jet-flex-view-react-example
npm install
```

#### 2. Run your project

After you created your project and cloned an example, make sure it works by running this command (or any other you use):

```
npm run start
```

![http://localhost:3000/](<../../../../.gitbook/assets/image (56) (1).png>)

The project works fine, so you can start developing your **JavaScript Component**. But before that, read the following step if you need the **Jet Admin API** integration.

{% hint style="warning" %}
Consider the following limitations while developing:

* You can't change the URL inside the Custom Component since the component is embedded using inside Jet Admin view
* Consider incapsulating styles inside your view, not using global styles
{% endhint %}

#### 3. (optional) Set up Jet API integration

To integrate your custom **JavaScript Component** with **Jet Admin** data and API, you can use the **Jet Admin SDK** library. To start using it, you would have to install it first:

```bash
npm install jet-admin-sdk
```

To work with **API** and perform queries, the **SDK** needs to know which **Project** you are working with and your **Access Token.** When a **Custom Component** is uploaded to production, it will fetch these automatically, but for development, you need to specify it manually, as shown below:

```javascript
import { getPublicApiService } from 'jet-admin-sdk';

if (!process.env.NODE_ENV || process.env.NODE_ENV === 'development') {
  getPublicApiService().projectsStore.setCurrent('YOUR_PROJECT_UNIQUE_NAME');
  getPublicApiService().authService.tokenLogin('YOUR_USER_TOKEN');
}
```

* **YOUR\_PROJECT\_UNIQUE\_NAME** – can be taken from the URL of your project on Jet Admin
* **YOUR\_USER\_TOKEN** – can be taken from the cookie token on [https://app.jetadmin.io/](https://app.jetadmin.io/)

That's it! You can now use **Jet Admin API** through **PublicApiService.** For example:

```typescript
import { getPublicApiService } from 'jet-admin-sdk';

getPublicApiService().currentUserStore.get().subscribe(result => {
  if (result) {
    console.log('Current User is ' + result.username);
  } else {
    console.log('Failed to get Current User');
  }
});
```

#### 4. Upload your JavaScript Component to Jet Admin

Once you're finished with your **JavaScript Component** or just want to test it in a real application, you need to upload it. Build your project first:

```bash
npm run build
```

Usually, it will create your build files in the **dist** folder, but it can differ for your environment. To upload your **Custom Component** to **Jet Admin,** you need to upload a **.zip** file with your build files. Go to the **dist** folder and compress all the contents to a single **.zip** file.

Now go to **Jet Admin** and create a **Custom Component** as shown below.

![](<../../../../.gitbook/assets/image (774).png>)

You will need to specify the following settings and click the **Save** button:

* **Compiled custom element** – a **zip** file containing your build files of **JavaScript Component**.
* **Custom element tag name** – tag name that you used for the **Web Component** inside your JavaScript Component project. Should be prefixed with "jet-" and has a dash-case. Also, each of your JavaScript Components should have unique tag names across your **Jet Admin** project.
* **Files to include in page** – for your JavaScript Component to work **JS** and maybe **CSS** files should be included. You should check which files from your **zip** files should be included. The order of loading can be changed. These files will be included only once when Custom Component should be displayed and after inclusion they must define a custom element with a tag name the same as you specified for the **Custom element tag name.**

![](<../../../../.gitbook/assets/image (775).png>)

![](<../../../../.gitbook/assets/image (776).png>)

{% hint style="success" %}
That's a wrap. Feel free to test your **Jet Admin** now.\
If you want to update it later, upload a new **.zip** file inside **Custom Component**.
{% endhint %}
