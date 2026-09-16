# Lists
Lists are great because they can serve many purposes and adapt
well to any kind of screen size. They can be used for browsing content,
navigation in a sidebar and much more.

## Rows
For the rows in a list Granite provides `Granite.ListItem`.
This makes sure your rows have consistent padding and size across all apps.
It also provides an API for the most common usage of a row. That is an icon (I plan to implement that),
a context menu, a label and a secondary description. Alternatively if you
need custom content you can set your own widget as a child.

## Placement
If the list is the only thing within its view (e.g. a sidebar or the entire window) it should be placed directly in the section.

![A list in a sidebar](https://elementary.io/images/docs/human-interface-guidelines/lists/settings-sidebar.png)

If a view contains other content in a Scrolled Window, add the style class
`Granite.CssClass.CARD` to the list and **do not** place it inside its own Scrolled Window.

Otherwise, if the list is the only scrollable content in the view, it should be placed
inside a Scrolled Window with `has_frame = true` .

At a glance, we can see that a list with either no frame or a card style frame means the whole view scrolls. A list with an inset frame means the list itself scrolls.

![Two lists using the `CARD` style](https://elementary.io/images/docs/human-interface-guidelines/lists/card-style.png)

## Actions
If you need to associate actions with the list (e.g. to add a new item)
you should put the list in a `Granite.ToolBox` and add a `Gtk.ActionBar`
on the bottom with flat buttons that use labels or symbolic icons.
The style should be `ToolbarStyle.RAISED`.

![A list inside a scrolled window with a frame and an action](https://elementary.io/images/docs/human-interface-guidelines/lists/frame-and-action.png)


## Adaptiveness
If the list was placed in a scrollable window with a frame the scrollable
window should be clamped. If it gets the CSS class `CARD` the list should
be clamped.

![Two lists using the `CARD` style being clamped](https://elementary.io/images/docs/human-interface-guidelines/lists/card-style.png)

If a list is the only Toolbox content—and therefore not within a frame—clamp the list and any top or bottom bars in the Toolbox separately.

Don't clamp the whole Toolbox. The separator separating the list content from the action bar will also be clamped.
