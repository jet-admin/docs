---
description: >-
  Turn any field into an AI-powered field that can automatically fill data using
  your instructions and your existing column values.
---

# AI Fields

AI Fields let you automate how data is generated or completed. You can convert a field into an AI Field, provide a short instruction (prompt), and let AI fill the column based on your instruction. AI Fields can work in bulk or update dynamically whenever input data changes.

#### Steps

1. **Convert a field to an AI Field:**\
   Open your table, hover over the column you want to automate, and click **Field Settings → Add AI auto fill**.
2.  **Add AI instruction:**\
    In the AI configuration panel, write a clear instruction for what the AI should do with your data.\
    Example:

    > “Fill here with random numbers from 10 to 50, and add a `$` sign next to each number."
3. **Enable advanced options (optional):**
   * **Enable Internet Search:** Allow AI to pull updated or related information from the web.
   * **Recalculate on inputs change:** Automatically refresh AI results whenever related columns are updated.
4. **Apply AI filling:**\
   After configuration, the AI can fill empty cells in that column automatically, either for the entire column at once, or individually when you click the AI icon in a cell.
5. **Review and refine results:**\
   You can manually adjust or overwrite AI-generated values at any time. All edits are saved instantly.

{% @arcade/embed flowId="jYhMFNfRnC10nFu53xhH" url="https://app.arcade.software/share/jYhMFNfRnC10nFu53xhH" %}

{% hint style="info" %}
**Tips for Better AI Results**\
• Keep instructions short and direct.\
• Enable **Recalculate on inputs change** for dynamic data.\
• Great for summarizing text, categorizing issues, or generating short responses from long descriptions.
{% endhint %}
