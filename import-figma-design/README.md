---
description: >-
  Design in Figma, launch in Jet. Turn your static designs into clean,
  production-ready code with the Figma to Jet plugin.
---

# 🖼 Import Figma Design

The Figma to Jet plugin lets you turn your static designs into clean, production-ready Jet HTML and CSS. Add Jet Interactions, wire up content using your data source, and one-click publish onto the fastest hosting infrastructure.\


### **Here’s how it works:**

1. **Install + connect.** Pass Figma Plugin key access to the Jet apps you’ll use to transfer designs from Figma to Jet.
2. **Copy + paste.** Design with auto layout in Figma, then easily translate your designs to Jet as responsive flexbox structures — you can even adjust HTML tags within Figma to get your app live faster.
3. **Polish + publish.** Bring your static designs to Jet, wire content with your data source, and one-click publish onto the fastest hosting infrastructure.

### **Additional features:**

* 20+ prebuilt layouts and responsive structures to smoothly convert to Jet — and are responsive across devices.
* Your styling, layouts, colors, text, and images will transfer seamlessly when you paste them into Jet.
* Automatic style guide creation — create a style guide page in Jet based off the text and color styles you’ve created in Figma.
* Support for exporting vectors nodes as SVGs.\


### What is not supported:

* Groups/Frames are ungrouped as multiple layers (will support soon)
* Auto layout (will support soon)
* Radial/Angular/Diamond gradients
* Shapes
* Custom border dashes
* Layer/Background blur
* Border join style

### **Workflow tips:**

* On paste, Jet class names will be derived from layer names. Jet automatically applies existing classes when the same styles are detected on an imported element.
* Pre-built layout and structure templates are built with auto layout and are fully responsive when pasted into Jet. It will not convert them to native Jet rows/columns or grids.
* All grouped layers and Vector layers will be exported as SVGs. This can be handy for complex multi-layer graphics.
* Prepend your text layers with \[H1]-- to apply HTML tags more quickly. This applies to headings \[H1-H6], paragraphs \[P] and links \[A].



### **Caveats and future improvements**

* All Jet classes are translated 1:1 with the names of the Figma frames. Due to the current copy/paste limitation on the Jet Component Designer, the plugin cannot detect whether a class is already used in Jet, which may lead to class duplication. The best workaround for this is removing instances of old Jet components, cleaning up unused styles, and repasting the designs. We plan on improving this workflow in the future.
* The plugin currently only supports copying of auto layout frames. We’re looking into supporting non-auto layout frames.
* The plugin doesn’t translate prototyping interactions from Figma. Users can apply Jet Interactions after pasting designs over.
* The plugin doesn’t transfer custom fonts. If you’re using custom fonts in Figma, you’ll need to upload them to your Jet site before copying.
* Instances are not supported. Detach instances before copying. Pro tip: clicking on the ⚠ icon will select all instances layers to make it easy to detach all at once.
* Jet color swatches will not be automatically created when copying over color styles from Figma. You’ll have to create the swatch after in Jet manually.



###
