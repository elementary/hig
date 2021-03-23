# Button

Buttons are an incredibly important widget to understand since your app will undoubtedly contain them.

## Tool Buttons

![Open button](https://elementary.io/images/docs/human-interface-guidelines/buttons/open.png)

### Labeling

Tool Buttons are almost always icon-only and do not provide a button border. They should not be accompanied by a label.

### Tooltips

All Tool Buttons should have tooltips, since they do not contain a label. This assists users with disabilities as well as giving a translation for an unrecognized icon. Tooltips should be done in [sentence case](../../reference/text.md#sentence-case) without [terminating punctuation](../../reference/text.md#terminating-punctuation).

Like text button labels, a tooltip should clearly describe what will happen when the button is pressed.

### **Keyboard Shortcuts**

If a button has a related keyboard shortcut that will perform the same action, its tooltip should include the shortcut. See [`Granite.markup_accel_tooltip ()`](https://valadoc.org/granite/Granite.markup_accel_tooltip.html) for specifics.

## Text Buttons

![Cancel button](https://elementary.io/images/docs/human-interface-guidelines/buttons/cancel.png)

### Labeling

Text Button labels should be done in [title case](../../reference/text.md#title-case).

Like menu items, Text Button labels should consist of an Action or a Location but not a status. Make sure that a button's label clearly describes what will happen when it is pressed.

"Remove Account", "Transfer to Jim's Laptop", and "Import 20 Songs" are good labels.

"OK", "Get more storage!", and "Low Battery" are not good button labels. The "Get more storage!" label has incorrect capitalization and unnecessary punctuation. The other two labels do not indicate what will happen as a result of clicking the button.

### Tooltips

Since Text buttons have a clear and explicit label, it's usually unnecessary to give them a tooltip.

{% hint style="info" %}
See also:

1. [Why The OK Button Is No Longer Okay](http://uxmovement.com/buttons/why-the-ok-button-is-no-longer-okay/) by UX Movement
2. [Should I use Yes/No or Ok/Cancel on my message box?](https://ux.stackexchange.com/questions/9946/should-i-use-yes-no-or-ok-cancel-on-my-message-box) on UX Stack Exchange
{% endhint %}

## Back Buttons

![Back Button](https://elementary.io/images/docs/human-interface-guidelines/buttons/back-button.png)

A back button is simply a text button with a special style class. It should be used to navigate back to a previous view, typically from a child view to the main view.

The text of the button should be the title of the previous view. If the button will take the user “home,” then “Home” may be an appropriate label; however a more specific label is preferred, such as “All Settings” in System Settings. Avoid just using “Back,” as the back button is visually distinct and going back is already implied by its unique shape. The button should tell the user _where_ it will take them back to.

When using a back button, it is recommended to use a Gtk.Stack to switch between views. This way you get a sliding animation further representing the backwards progression when activating the back button.

Back buttons are typically seen in header bars, but can be used in other contexts as well.

