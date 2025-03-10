---
description: >-
  Easily integrate custom fonts into Jet Admin using Global CSS by uploading
  font files, linking them, and applying them globally.
---

# Adding Custom Fonts

### **Step 1: Upload Font Files to Storage**

1. Navigate to **Storage** in Jet Admin.
2. Create a new folder for your font files (e.g., `Fractul`).
3. Upload all the required font files into this folder.

In the example below, the font files for "Fractul" are uploaded with different styles and weights such as:

* Fractul-Black.ttf
* Fractul-Bold.ttf
* Fractul-Italic.ttf
* Fractul-Light.ttf
* etc.

{% @arcade/embed flowId="OpwqR9w0HjBwbl6Ktu4i" url="https://app.arcade.software/share/OpwqR9w0HjBwbl6Ktu4i" %}

### **Step 2: Get the File Path**

To get the correct file path for your font:

1. Click on the file in **Storage**.
2. In the details panel, click on the **File Name**.
3. This will open the file in a new tab.
4. The URL of this new tab is the direct path to the file, which you can use in your custom code.

{% @arcade/embed flowId="GlPf9oFAUgil50VxleX6" url="https://app.arcade.software/share/GlPf9oFAUgil50VxleX6" %}

### **Step 3: Define Fonts in Global CSS**

Now that the font files are uploaded and you have your file paths, you can define them in Global CSS.

1. Navigate to **App Settings** in Jet Admin.
2. Go to **Global CSS**.
3. Paste the following CSS, adjusting the links according to the file paths you obtained:

```
@font-face {
  font-family: 'Fractul';
  font-style: normal;
  font-weight: 900;
  src: url('YOUR_FILE_PATH/Fractul-Black.ttf') format('truetype');
}

@font-face {
  font-family: 'Fractul';
  font-style: italic;
  font-weight: 900;
  src: url('YOUR_FILE_PATH/Fractul-BlackItalic.ttf') format('truetype');
}

@font-face {
  font-family: 'Fractul';
  font-style: normal;
  font-weight: 700;
  src: url('YOUR_FILE_PATH/Fractul-Bold.ttf') format('truetype');
}

@font-face {
  font-family: 'Fractul';
  font-style: italic;
  font-weight: 700;
  src: url('YOUR_FILE_PATH/Fractul-BoldItalic.ttf') format('truetype');
}

/* Add more font styles as needed */

body {
  --regular-font: 'Fractul', sans-serif;
  --heading-font: 'Fractul', sans-serif;
}
```

{% @arcade/embed flowId="Q7C4qHr8c0lmCsBhLs6j" url="https://app.arcade.software/share/Q7C4qHr8c0lmCsBhLs6j" %}

{% hint style="info" %}
Each font file URL should be copied directly from the file path found in **Step 2**. For example, if you uploaded your fonts to a folder called `Fractul`, the link for `Fractul-Black.ttf` would be:

```
https://cdn-api.jetadmin.app/media/static_files/projects/YOUR_PROJECT/Fractul/Fractul-Black.ttf
```

Make sure to replace `YOUR_FILE_PATH` with the exact file path copied from your storage.
{% endhint %}

### **Step 4: Reset Font to Default**

If the font does not appear correctly, reset it by:

1. Going to **App Settings** > **Global CSS**.
2. Removing any existing font settings.
3. Saving and refreshing the page.

{% hint style="info" %}
### **Download Full CSS Code**

For the complete CSS code, download this file below, copy the code, and paste it into your **Global CSS**. Don't forget to update the file paths for each URL.
{% endhint %}

{% file src="../../../../.gitbook/assets/Custom font Css.txt" %}

If you face any issues or need assistance, feel free to contact our support team.
