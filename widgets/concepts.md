---
description: Basic concepts that apply to all widgets
---

# Concepts

Before we get into all the widgets available in elementary OS, we need to cover some basic concepts that apply to all widgets. Employing these concepts correctly will create a more seamless experience for your users and help you avoid sifting through bug reports!

## Avoid Widgets That Do Nothing

Interfaces should aim to provide an obvious response to interaction. When an actionable widget seemingly does nothing, this creates confusion and can even be scary for curious new users who are still exploring your app—Think, "uh-oh I don't know what happened!". There are two common ways to avoid widgets that do nothing: setting their sensitivity or hiding them.

Making a widget insensitive informs the user that the functionality is available, but only after a certain condition is met. Hiding a widget is more useful when it doesn't make sense in a given context, or when it would help the UI to feel less overwhelming.

{% hint style="warning" %}
Keep in mind that insensitive items will still be recognized by screen readers and other assistive tools, while hidden widgets will not.
{% endhint %}

### Set Sensitivity For Widgets With Prerequisites

Sometimes it doesn't make sense for a user to interact with a widget until some prerequisite is fulfilled. For example, It doesn't make sense to let a user click a browser's "Forward" button unless there is forward history available. In this case, you should make the "Forward" button insensitive or a user may click it, expecting a result, and be confused when nothing happens. A disabled button at the end of a form can help convey that all required fields haven't been filled out yet. A disabled view can draw visual attention to an associated switch that activates a required feature.

{% hint style="info" %}
All GTK widgets inherit the property [`sensitive`](https://valadoc.org/gtk+-3.0/Gtk.Widget.sensitive.html).
{% endhint %}

### Hide Widgets That Aren't Useful In The Current Context

When a widget only makes sense in a certain context \(not as an indicator of an action to be performed\) it often makes more sense to hide it. Take hardware requirements for example: It may not make sense to show multi-display options if the system only has a single display. Making multi-display options insensitive is not really a helpful hint in this context and also serves to add complexity and clutter to your UI.

Consider the "clear" button present in [search fields](ui-toolkit-elements/#search-fields). This button only appears when it is relevant and needed. Setting this button as insensitive only clutters the UI since it's not important to hint to the user that this entry can be quickly cleared once there is text in it.

{% hint style="warning" %}
Hiding a widget can give the impression that functionality is not available at all or can leave a user wondering why a feature has suddenly "disappeared". Be sure that this widget isn't necessary as an affordance.
{% endhint %}

GTK widgets can be hidden with the property [`visible`](https://valadoc.org/gtk+-3.0/Gtk.Widget.visible.html), but it's usually nicer to pack them into a [revealer](https://valadoc.org/gtk+-3.0/Gtk.Revealer.html) in order to provide animations.

## Spacing

* Windows should have a 12px \(minimum\) space between any widgets and the window's border.
* Labels should be 12px \(minimum\) from their widgets.
* If there are section headers present, labels should be indented.
* Horizontal spacing between buttons is 6px.

## Alignment

* Widgets should be "Justified" so that they align on both the left and right sides. Do not include "descriptor" widgets such as icons or labels in this justification.
* Labels should be right aligned with respect to each other when possible.
* Section headers should be left aligned with respect to each other.

{% hint style="info" %}
See also: [Form Label Proximity: Right Aligned is Easier to Scan](http://uxmovement.com/forms/form-label-proximity-right-aligned-is-easier-to-scan) by UX Movement
{% endhint %}

