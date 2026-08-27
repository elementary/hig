# Lists
Lists are great because they can serve many purposes and adapt
well to any kind of screen size. They can be used for browsing content,
navigation in a sidebar and much more.

## Rows
For the rows in a list Granite provides `Granite.ListItem`.
This makes sure your rows have consistent padding and size across all apps.
It also provides an API for the most common usage of a row. That is an icon (I plan to implement that),
a label and a secondary description. Alternatively if you need custom
content you can set your own widget as a child.

## Placement
If the list is the only thing within its section (e.g. a sidebar or the entire window)
it should be placed directly in the section. If it sits alongside other content
it should be placed inside a `Gtk.Frame` or a `Gtk.ScrolledWindow` with
`has_frame = true`.

TODO: Screenshots of both.
Appcenter Installed View + a sidebar from e.g. settings for directly in the section
A settings page e.g. connected devices in the power settings for in a frame

## Actions
If you need to associate actions with the list (e.g. to add a new item)
you should put the list in a `Granite.ToolBox` and add a `Gtk.ActionBar`
on the bottom with flat buttons that use labels or symbolic icons.
The style should be `ToolbarStyle.RAISED`.

## Adaptiveness
If the list was placed in a frame the frame should be clamped.

If it is the only thing in its section and therefore not within a
frame the actual list should be clamped and, if it's used, the
action bar should be clamped separately. You shouldn't
clamp the whole toolbar because then the separator
separating the list content from the action bar will also
be clamped which looks weird.

TODO: Screenshots
Appcenter Installed view for clamping the lsit
A settings page for clamping the frame

## CssClass.CARD?
TODO: When to use this? I've seen it used where elsewhere
with the same function something else was used.
E.g. in the bluetooth settings the device list uses CARD but in network settings
the networks list uses a list in a frame.
IMO using list in a frame makes more sense for dynamic lists like that.

I think card should maybe only be used for static list i.e. lists
where the number of rows don't change? The style seems similar to
adw.preferencesgroup so that's why I thought only for static items.
