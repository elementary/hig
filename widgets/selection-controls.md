# Selection Controls

Selection controls present a way for users to select or enable options. There are several types of selection controls available in elementary OS:

* **Checkboxes** present a way for users to select multiple items from a set.
* **Comboboxes** and **Radio buttons** present a way for users to select a single option from a set.
* **Linked buttons** present a compact way for users to select options that can be described by an icon or with only one or two words.
* **Switches** present a way for users to toggle certain features or behaviors "on" or "off".

## Checkboxes

![Checkboxes](https://elementary.io/images/docs/human-interface-guidelines/selection-controls/checkboxes.png)

Use checkboxes when users are making a selection of items. If you have a single option, avoid using a checkbox and use a switch instead.

Make sure that users can toggle the state of the checkbox by clicking on the label associated with the checkbox.

Labels associated with checkboxes should usually be nouns or nounal phrases.

## Comboboxes

![Comboboxes](https://elementary.io/images/docs/human-interface-guidelines/selection-controls/comboboxes.png)

Use a combobox \(also called a dropdown\) when:

* Users are selecting only a single item from a set and
* The set is too long to show all available options at once

## Linked Buttons

![Linked Buttons](https://elementary.io/images/docs/human-interface-guidelines/selection-controls/linked_buttons.png)

Use linked buttons when:

* All options can be described by an icon or with only one or two words and
* You think users should see all available options at once.

Linked buttons can be used to select multiple related options like "Bold", "Italic", and "Underline", or they can be used to select a single mutually exclusive option \(also called a mode button\) like Grid, List, or Column view.

Linked buttons should never contain colored icons. Only 16px symbolic icons OR text. Do not mix icons and text.

## Radio Buttons

![Radio Buttons](https://elementary.io/images/docs/human-interface-guidelines/selection-controls/radio_buttons.png)

Use radio buttons when:

* Users are selecting only a single item from a set and
* You think users should see all available options at once.

## Switches

![Switches](https://elementary.io/images/docs/human-interface-guidelines/selection-controls/switches.png)

Use a switch when users are toggling certain features or behaviors "on" or "off".

Don't use switches to select related items as part of a list, instead use a checkbox. Think of switches as acting on independent services and checkboxes as including objects in a list. This is an important distinction to make.

When possible, directly call out the service you are acting on. Do not use words that describe the state that the widget is describing like "Enable Multitouch", "Use Multitouch", or "Disable Multitouch". This can create a confusing situation logically. Instead, simply use the noun and write "Multitouch".

### Mode Switches

![Mode Switches](https://elementary.io/images/docs/human-interface-guidelines/selection-controls/mode-switches.png)

As of elementary OS 5 Juno, mode switches are a new switch-based widget that communicate switching between two distinct states. For example, switching between a photo or video mode in a camera. The switch is drawn smaller and inline with the provided symbolic icons. Tooltip hints can also be provided when hovering the icons.

Use a mode switch when you have two distinct and opposing states that you are switching between that can be effectively communicated via an icon. If you need text or more than two states, use [grouped ToggledButtons](https://valadoc.org/gtk4/Gtk.ToggleButton.group.html) instead.

{% hint style="info" %}
_See also:_ [_3 Ways to Make Checkboxes, Radio Buttons Easier to Click_](http://uxmovement.com/forms/ways-to-make-checkboxes-radio-buttons-easier-to-click/) _by UX Movement_
{% endhint %}



