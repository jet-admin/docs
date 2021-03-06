# Flex View

## What is a Flex View?

For very specific pages you can create your own custom **FlexView** based on **React,** **Angular** or any other framework and integrate it in **Jet Admin** interface. Writing your own custom **JS/CSS/HTML** has no limits in implementing any page you need.

To integrate your custom **FlexView** with **Jet Admin** data you can use **Jet Admin SDK** library.

## Create Flex View

In this tutorial we'll show you how to create a sample Flex View component which you can later on extend to satisfy whatever needs you have.

#### 1. Create your FlexView component project \(playground\) or clone an example

A Flex View uses [Web Component](https://www.webcomponents.org/introduction) specification to integrate any **JS** based component to **Jet Admin** – this allows you to use any **Frameworks** and **Libraries** you like as long as you create them as custom **Web Components**. So it can be **React**, **Angular**, **Vue.js** based components or any other.

First, you need to create a **FlexView** project where you can develop and test it. This project will be your playground for creating **FlexView**. It will work the same way as on **Jet Admin** but will make your development easier so that you can use your favourite **IDE** and environment. To make it simpler, you can use some of our ready-to-use starter projects on **GitHub** or use them as a reference:

* React – [https://github.com/jet-admin/jet-flex-view-react-example](https://github.com/jet-admin/jet-flex-view-react-example)
* Angular – [https://github.com/jet-admin/jet-flex-view-angular-example](https://github.com/jet-admin/jet-flex-view-angular-example)

For example, here's an example of cloning React and preparing it for work:

```bash
git clone git@github.com:jet-admin/jet-flex-view-react-example.git
cd jet-flex-view-react-example
npm install
```

#### 2. Run your project

After you created your project and cloned an example, make sure it works by running this command \(or any other you use\):

```text
npm run start
```

![http://localhost:3000/](../../.gitbook/assets/image%20%2812%29.png)

The project works fine, which means that you can start developing your **FlexView**. But before that, read the following step if you need the **Jet Admin API** integration.

{% hint style="warning" %}
Consider the following limitation while developing:

* You can't use change URL inside FlexView since component is embed inside Jet Admin view
* Consider incapsulating styles inside your view, not use global styles
{% endhint %}

#### 3. \(optional\) Set up Jet API integration

To integrate your custom **FlexView** with **Jet Admin** data and API, you can use **Jet Admin SDK** library. To start using it, you would have to install it first:

```bash
npm install jet-admin-sdk
```

To work with **API** and perform queries, the **SDK** needs to know which **Project** you are working with and your **Access Token.** When a **FlexView** is uploaded to production, it will fetch these automatically, but for development you need to specify it manually as shown below:

```javascript
import { getPublicApiService } from 'jet-admin-sdk';

if (!process.env.NODE_ENV || process.env.NODE_ENV === 'development') {
  getPublicApiService().projectsStore.setCurrent('YOUR_PROJECT_UNIQUE_NAME');
  getPublicApiService().authService.tokenLogin('YOUR_USER_TOKEN');
}
```

* **YOUR\_PROJECT\_UNIQUE\_NAME** – can be taken from URL of your project on Jet Admin
* **YOUR\_USER\_TOKEN** – can be taken from cookie token on [https://app.jetadmin.io/](https://app.jetadmin.io/)

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

####  4. Upload your FlexView to production

Once you're finished with your **FlexView** or just want to test it in a real application, you need to upload it. Build your project first:

```bash
npm run build
```

Usually, it will create your build files in **dist** folder, but it can differ for your environment. To upload your **FlexView** to **Jet Admin,** you need to upload a **.zip** file with your build files. Go to **dist** folder and compress all the contents to a single **.zip** file.

Now go to the **FlexView** create page as shown below.  
\(Project Settings → FlexViews → Create FlexView\)

![](../../.gitbook/assets/image%20%28182%29.png)

![](../../.gitbook/assets/image%20%28205%29.png)

![](../../.gitbook/assets/image%20%28153%29.png)

Fill in the form and click the **Create** button:

* **Unique Tag Name** – tag name that you used for **Web Component** inside your **FlexView** project. Should pre prefixed with "jet-" and has dash-case. Also each of your **FlexView** should have unique tag names across your **Jet Admin** project.
* **Display Name** – name of **FlevView** used in **Jet Admin** interface.
* View Type – affects where **FlexView** will be visible, has the following options:
  * **Common** – can be added as a link to menu as an independent page
  * **Collection** – will be visible as a link on top of **Collection** list pages. **Collection** name will be passed to this **FlexView** as a parameter.
  * **Record** – will be visible as a link on top of **Record** view/change pages. **Collection** name and **Record** primary key will be passed to this **FlexView** as parameters.
* **Collection** – only of **Collection** and **Record** view types. Can limit for which **Collection** this **FlexView** will be visible. Can be set to **any**.
* **Compiled custom element** – **zip** file containing your build files of **FlexView**.
* **Files to include into page** – in order for your **FlexView** to work **JS** and maybe **CSS** files should be included. You should check which files from your **zip** files should be included. The order of loading can be changed. These files will be included only once when **FlexView** should be displayed and after inclusion they must defined custom element with tag name the same as your specified for **Unique Tag Name**.

{% hint style="info" %}
For static media files use the following base URL:  
[https://api.jetadmin.io/media/custom\_views/PROJECT\_NAME/FLEX\_VIEW\_NAME/](https://api.jetadmin.io/media/custom_views/PROJECT_NAME/FLEX_VIEW_NAME/)
{% endhint %}

{% hint style="success" %}
That's a wrap. Feel free to test your **FlexView** now.  
If you want to update it later, you can go to _Project Settings → FlexViews → Your FlexView_ and change the settings or upload a new **.zip** file.
{% endhint %}

![Common FlexView example](../../.gitbook/assets/image%20%28248%29.png)

![Collection FlexView example](../../.gitbook/assets/image%20%2830%29.png)

![Record FlexView example](../../.gitbook/assets/image%20%28240%29.png)

## Common Problems

### FlexView is not being loaded showing blank page

If you are using multiple **FlexView** in your project there can be an issue with **Webpack Entrypoint** conflict because of using the same name for **webpackJsonp** function. 

If this is the case, then you need to set different **webpackJsonp** function name for different **FlexView**. This can be achieved by setting **Webpack** configuration:

```javascript
module.exports = {
  output: {
    jsonpFunction: 'webpackYourCustomJsonp'
  }
};
```

####  For Angular

You can check example project on GitHub with custom jsonpFunction  
[https://github.com/jet-admin/jet-flex-view-angular-example](https://github.com/jet-admin/jet-flex-view-angular-example)

or

To update existing project to use custom webpackJsonp function:

1. Install **ngx-build-plus** by running

```javascript
npm install --save ngx-build-plus
```

2. Update **angular.json** to use **ngx-build-plus** build option

{% code title="angular.json" %}
```javascript
{
  "$schema": "./node_modules/@angular/cli/lib/config/schema.json",
  "version": 1,
  "newProjectRoot": "projects",
  "projects": {
    "example-project": {
      ....
      "architect": {
        "build": {
          // Set it here
          "builder": "ngx-build-plus:build",
          ...
        }
      }
    }
  }
}
```
{% endcode %}

 3. Update build command in **package.json** to include **webpack.extra.js**

{% code title="package.json" %}
```javascript
{
  "name": "example-project",
  "version": "0.0.1",
  "scripts": {
    ...
    "build": "ng build --prod --extra-webpack-config webpack.extra.js",
    ...
  }
}
```
{% endcode %}

 4. Add **webpack.extra.js** in root folder and set **jsonpFunction** to unique name for every **FlexView**:

{% code title="webpack.extra.js" %}
```javascript

module.exports = {
  output: {
    jsonpFunction: 'webpackYourCustomJsonp'
  }
};
```
{% endcode %}

 

