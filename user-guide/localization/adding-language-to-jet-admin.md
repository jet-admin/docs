---
description: 'To add a new language to Jet Admin, follow these steps:'
---

# Adding Language to Jet Admin

{% hint style="warning" %}
**Requirements:** Ensure you have a good understanding of both the source language (English) and the target language. Familiarity with GitHub and version control systems is also beneficial for submitting changes via Pull Requests.
{% endhint %}

### **Accessing GitHub Files:**&#x20;

Access the necessary files from the [Jet Admin Localization GitHub Repository](https://github.com/jet-admin/jet-localization). You'll need to create new files, and push them as a 'Pull Request'. Our GitHub repository hosts a collection of files used for localization.

### **Understanding File Structure:**&#x20;

In the root folder, you'll find a folder containing files for email templates and individual files for each language. Each language file is named in the format `locale.xx.ts`, where "xx" represents the language code (e.g., `locale.en.ts` for English, `locale.fr.ts` for French).

<figure><img src="../../.gitbook/assets/Screenshot 2024-03-14 234434.jpg" alt=""><figcaption></figcaption></figure>

### **Translating Content:**&#x20;

Open the desired language file (e.g., `locale.es.ts` for Spanish). These files contain lines with the English term followed by its translation in the respective language. For example:

```
{ source: 'Save', target: 'sauvegarder' },
{ source: 'Create', target: 'Créer' },
...
```

Simply copy this file, rename it to `locale.xx.ts` (replace "xx" with the language code of your choice), and replace the Spanish translations with the corresponding translations in the new language.

### **Email Templates:**&#x20;

Apart from the main localization file, there are additional pages for email templates that need translation. These pages are named "email\_verification", "project\_user\_invitation", and "user\_restore".

<figure><img src="../../.gitbook/assets/Screenshot 2024-03-14 235031.jpg" alt=""><figcaption></figcaption></figure>

### **Scope of Work:**&#x20;

The translation task may involve numerous lines of text. For instance, the Spanish file contains 557 lines, although not all may require translation. Use this as a reference for the scope of work.

### **Localization Submission:**&#x20;

Once you've finished translating the files, feel free to send us your work through a 'Pull Request' on GitHub. Don't forget to include a description of what you've changed. Although we're not actively creating new translations ourselves, we'd still love to see your localization and add it! Looking forward to seeing what you've got!

{% hint style="success" %}
By following these steps, you can effectively add a new language to Jet Admin.
{% endhint %}
