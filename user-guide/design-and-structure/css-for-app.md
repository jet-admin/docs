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

****![](<../../.gitbook/assets/image (1).png>)****

```css
[data-component-id="{text-component-id}"] .text-truncate{
    text-align: center;
    font-size: 40px;
    color: black;
}
```

****

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

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption><p> ()</p></figcaption></figure>

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
