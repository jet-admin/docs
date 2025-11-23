---
description: >-
  Connect Google Translator to JetAdmin to detect languages, list supported
  languages, and translate text directly in your app or workflows.
---

# Google Translator

The **Google Translator resource** lets you use Google Cloud Translation inside JetAdmin. After connecting with your API key, you can run translation operations, detect languages from text input, and retrieve the list of languages supported by Google Translate.\
This is perfect for multilingual apps, content generation workflows, support tools, and automated translation tasks.

#### Steps

1. **Go to Data Settings:**\
   In JetAdmin, open **Data → Add Resource**.
2. **Select Google Translator:**\
   Choose **Google Translator** from the list of available data sources.
3. **Name your resource (optional):**\
   Give it a custom name like _Translator API_ or _Language Tools_.
4. **Paste your Google API Key:**\
   Enter your Google Cloud Translation API key.\
   &#xNAN;_&#x4E;ote: The Translation API must be enabled in your Google Cloud console._
5. **Add Resource:**\
   JetAdmin will validate your key and complete the setup, making translation actions immediately available.

{% @arcade/embed flowId="zujfQwpMWAeSb05lDgNI" url="https://app.arcade.software/share/zujfQwpMWAeSb05lDgNI" %}

{% hint style="info" %}
**Actions Overview**\
Once connected, JetAdmin provides three key translation actions:\
• **Detect Language:** Identify the language of any given text.\
• **Get Supported Languages:** Retrieve a full list of languages supported by Google Translate.\
• **Translate Text:** Translate text from one language to another using Google’s neural machine translation.
{% endhint %}

