# Search Entry

Apps that support the searching or filtering of content should include a search entry on the right side of the app's toolbar. This gives users a predictable place to see whether or not an app supports searching, and a consistent location from which to search. GTK provides a convenient complex widget for this purpose called [Gtk.SearchEntry](https://valadoc.org/gtk+-3.0/Gtk.SearchEntry.html).

![Search Field](https://elementary.io/images/docs/human-interface-guidelines/search-fields/search-field.png)

## Distinguish Between Search and Find

Search is for filtering the contents of a library, i.e. Music or Videos, to the matching items. Search is typically initiated when typing anywhere in a library view.

Find is for highlighting matching instances of a string, i.e. in a text editor, web page, or Terminal. It is triggered by a keyboard shortcut \(Ctrl+F\) or with a search icon. The find bar appears in a revealer below the header bar with relevant actions such as find next, find previous, highlight all, etc. The revealer may also contain other relevant actions such as replace or go to line.

## Behavior

If it is possible to include search functionality within your app, it is best to do so. Any list or representation of multiple pieces of data should be searchable using a search field that follows these rules:

* Results should be instantly shown as you type. This helps your app to appear faster and is more useful than having to hit "Enter" and wait. Exceptions may be made if the data is not stored locally.
* In most cases, the search should be case-insensitive; users should not be expected to provide the exact capitalization. A good compromise is "smart case" where case is respected whenever the user intentionally types lower and upper case letters.

## Labeling

Search fields should contain hint text that describes what will be search. You can set this using the entry property ["placeholder\_text"](https://valadoc.org/gtk+-3.0/Gtk.Entry.placeholder_text.html).

Most search fields should use the format "Search OBJECTS" where OBJECTS is something to be searched, like Contacts, Accounts, etc.

If the search field interacts with a search service, the hint text should be the name of that service such as "Google" or "Yahoo!"

