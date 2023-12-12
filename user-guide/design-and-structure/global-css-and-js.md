---
description: Customize the way your app looks
---

# Global CSS & JS

Custom CSS and Javascript allow you to enhance your branding and UI/visual tweaks, without completely changing the look and feel of your app. For example, you can use Custom CSS to change the style of the components: colors,  size, text alignment, etc.

**Using Custom CSS & JS:**

{% embed url="https://www.loom.com/share/5ee5e1c2f92b4228b97d3c4f6d894831" %}

Custom CSS and JS are used in the same way for the app and the  Sign in/Sign up page, but they are configured independently. The Custom CSS/JS settings can be accessed in the Scripts & Styles sections of the App Settings and Sign in & Sign up menus.&#x20;

1. Go to App Settings or Sign in & Sign up menu

<figure><img src="../../.gitbook/assets/Снимок экрана 2023-04-11 в 20.17.53.png" alt=""><figcaption><p>App Settings menu location</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Снимок экрана 2023-04-11 в 20.14.21.png" alt=""><figcaption><p>Sign in/Sign up menu location</p></figcaption></figure>

2\. Go to **Scripts & Styles** in the menu and paste your CSS or JS in the appropriate in **Global CSS** or **Global Javascript** field.

<figure><img src="../../.gitbook/assets/Снимок экрана 2023-04-11 в 20.21.10.png" alt=""><figcaption><p>Scripts &#x26; Styles menu section</p></figcaption></figure>

### Menu Style

<figure><img src="../../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

Update menu background color:

```css
.admin-header{
    background-color:#C4CDFB;
}

.admin-header-link__label{
    color:#000;
    text-size:18px;
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

### **Detail. Text Font and Size**

![](<../../.gitbook/assets/image (1) (1) (3).png>)

![](<../../.gitbook/assets/image (1) (1) (3).png>)

```css
[data-component-id="{text-component-id}"] .text-truncate{
    text-align: center;
    font-size: 40px;
    color: black;
}
```





### Input Text Field Style

```css
.field__label {
    display: block;
    font-size: 16px;
    text-transform: uppercase;
    margin-bottom: 8px;
    margin-top: 8px;
    color: #2B50ED;
}

.field__content {
    font-size: 16px;
    color: #2B50ED;
}
```

### Table Row Style (Selected row color)

<figure><img src="../../.gitbook/assets/image (2) (1) (3).png" alt=""><figcaption><p> ()</p></figcaption></figure>

```css
.table__row_selected:nth-child(2n) {background: red !important;}
.table__row_selected:nth-child(2n+1) {background: red !important;}

.table__row_selected:nth-child(2n), .table_openable .table__row_selected:hover:nth-child(2n) {
    background:#04CFC9 !important
}

.theme_dark .table__row_selected:nth-child(2n), .theme_dark .table_openable .table__row_selected:hover:nth-child(2n) {
    background:#2b50ed !important
}

.table__row_selected:nth-child(2n + 1), .table_openable .table__row_selected:hover:nth-child(2n + 1) {
    background:#04CFC9 !important
}

.theme_dark .table__row_selected:nth-child(2n + 1), .theme_dark .table_openable .table__row_selected:hover:nth-child(2n + 1) {
    background:#2a4acf !important
}
```
