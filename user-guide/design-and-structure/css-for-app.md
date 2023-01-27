---
description: Customize the way your app looks
---

# CSS for App

Custom CSS allows you to enhance your branding and UI/visual tweaks, not completely changing the look and feel of your app. For example, you can use Custom CSS to change the style of the components: colors,  size, text alignment, etc.

{% embed url="https://www.loom.com/share/5ee5e1c2f92b4228b97d3c4f6d894831" %}

1. Go to App Settings

<figure><img src="../../.gitbook/assets/Screenshot 2023-01-26 at 17.17.24.png" alt=""><figcaption></figcaption></figure>

2\. Choose Scripts & Styles and paste your CSS in **Global CSS**

<figure><img src="../../.gitbook/assets/global23 (1).jpg" alt=""><figcaption></figcaption></figure>

#### Update Menu Style

Update menu background color:

```css
.admin-header {
    background-color: yellow;
}
```



Update menu item style:

```css
.admin-header__title {
    font-size: 16px;
    color: #2B50ED;
    text-align: center;
}
```

