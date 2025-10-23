---
description: >-
  Turn any field into an AI-powered field that can automatically fill data using
  smart instructions and your existing column values.
hidden: true
---

# AI Fields

AI Fields in JetAdmin let you automate how data is generated or completed. You can convert a field into an **AI Field**, provide a short instruction (prompt), and let AI fill the column based on your instruction. AI Fields can work in bulk or update dynamically whenever input data changes.

#### Steps

1. **Convert a field to an AI Field:**\
   Open your table, hover over the column you want to automate, and click **Field Settings → Add AI auto fill**.
2.  **Add AI instruction:**\
    In the AI configuration panel, write a clear instruction for what the AI should do with your data.\
    Example:

    > “Summarize the issue reported in the **Description** column in one short sentence.”\
    > For instance, if your _Description_ field contains:\
    > “User reports that some of their video thumbnails rotated 90 degrees counter-clockwise, but the videos themselves are fine.”\
    > The AI field could automatically generate:\
    > “Video thumbnails are rotated incorrectly, but playback works normally.”
3.  **Reference other columns:**\
    Use your existing columns (like _Description_, _Category_, or _User Name_) in your AI instruction.\
    Example:

    > “Generate a short summary of the **Description** and categorize the issue as visual, functional, or other.”
4. **Enable advanced options (optional):**
   * **Enable Internet Search:** Allow AI to pull updated or related information from the web.
   * **Recalculate on inputs change:** Automatically refresh AI results whenever related columns are updated.
5. **Apply AI filling:**\
   Once configured, AI will automatically fill empty cells in that column, either all at once or one by one as you review each record.
6. **Review and refine results:**\
   You can manually adjust or overwrite AI-generated values at any time. All edits are saved instantly.

<mark style="color:$danger;">arcade</mark>

{% hint style="info" %}
**Tips for Better AI Results**\
• Keep instructions short and direct.\
• Use clear column references (e.g., `{Description}`, `{Category}`).\
• Enable **Recalculate on inputs change** for dynamic data.\
• Great for summarizing text, categorizing issues, or generating short responses from long descriptions.
{% endhint %}
