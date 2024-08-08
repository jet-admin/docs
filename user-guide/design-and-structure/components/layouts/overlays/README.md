# Overlays

Overlays, also known as Modals are windows — both large and small that “pop” onto the screen when an action is taken. Sometimes these come in the form of a warning (e.g. “Are you sure you want to delete that?”) and sometimes they can be in the form of something useful (e.g. clicking a "view details" button and seeing the specifics about an object).

Jet Admin provides 3 types of overlays:

1. Modals. Opens above page content in the center of the screen.
2. Slideouts. Slides outs from the side of the screen over page content.
3. Dropdowns. Dropdown next to click origin over page content.

To set up an `Overlay`, follow the steps:

1. Click on the `Overlays` Tab from the top bar
2. Click `+` on the Add Button near a modal, slideout of dropdown
3. Click on the `Customize` button
4. Choose the Style you want to use

{% @arcade/embed flowId="2lGL2xo2EeysgXzxEf6A" url="https://app.arcade.software/share/2lGL2xo2EeysgXzxEf6A" %}

You can customize your Modals by showing a close button and enabling closure when clicking the background overlay.

{% content-ref url="customizing-overlay.md" %}
[customizing-overlay.md](customizing-overlay.md)
{% endcontent-ref %}

You can pass dynamic parameters from the page into your Modals, allowing you to populate them with contextual data.

{% content-ref url="overlay-parameters.md" %}
[overlay-parameters.md](overlay-parameters.md)
{% endcontent-ref %}

Modals support adding custom actions, giving you the flexibility to build interactive workflows.

{% content-ref url="building-dynamic-workflows.md" %}
[building-dynamic-workflows.md](building-dynamic-workflows.md)
{% endcontent-ref %}
