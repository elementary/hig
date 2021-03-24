---
description: The primary method of discovering and using your app
---

# App Launcher

An app launcher file (or .desktop file) contains information that will be used to display your app when it is installed, such as in the Applications menu and Dock. It contains an app's name, description, categories, icon, keywords, and associated actions.

{% hint style="info" %}
For technical information about shipping app launcher files see our [developer documentation](https://docs.elementary.io/develop/writing-apps/our-first-app#the-desktop-file)
{% endhint %}

The naming and description portion of the app launcher file should follow this formula:

_**Name** is a\(n\) **GenericName** that helps you **Comment**._

```text
Name=Eddy
GenericName=Package Installer
Comment=Install Debian packages
```

## Name

You should not include descriptive words in your app's `Name`. For example, an address book app might be called "Dexter," not "Dexter Address Book." A web browser might be called "Midori," but not "Midori Web Browser." Instead, use the `GenericName` attribute of your app's .desktop file for a generic name, and the `Comment` attribute for a longer descriptive phrase.

```text
Name=Dexter
```

## GenericName

If your app is easily categorized or described with a generic name, you should use that for the GenericName attribute in your app's .desktop file. If you can say, "My app is a\(n\) _\*\*\_\_\*\*\_," then whatever fits in that blank could be the generic name. For example, Quilter is a markdown editor, so its generic name is "Markdown Editor".

You should not include articles \(the, a, an\) or the words "program," "app," or "application" in your app's generic name.

The generic name should be in [title case](./#title-case) and may be used around the system to better describe or categorize your app:

```text
GenericName=Markdown Editor
```

## Comment

The system uses an app's Comment attribute \(found in the .desktop file\) to succinctly inform a user what can be done with the app. It should be a short sentence or phrase beginning with a verb and containing the primary nouns that your app deals with. For example, the following are appropriate comments:

* Calendar: **Browse and schedule events**
* Mail: **Send and receive mail**
* Files: **Browse and manage your files**

An app's comment should be in [sentence case](./#sentence-case), not include terminal punctuation \(periods, exclamation points, or question marks\), and should be as short as possible while describing the _primary_ use case of the app:

```text
Comment=Listen to music
```

## Categories

Categories are used to sort your app in AppCenter and in the applications menu. In your app launcher file, they should be separated by and terminated with a semicolon:

```text
Categories=Graphics;Photography;Viewer;
```

The full list of supported categories can be found in the FreeDesktop.Org [menu entry](https://specifications.freedesktop.org/menu-spec/latest/apa.html) specification and the [list of additional categories](https://standards.freedesktop.org/menu-spec/latest/apas02.html)

{% hint style="info" %}
You can add more than one category to your app launcher file and you should add all that apply
{% endhint %}

## Keywords

You may also include keywords in your launcher to help users find your app via search. These follow [the "Keywords" key](https://standards.freedesktop.org/desktop-entry-spec/latest/ar01s05.html) in your .desktop file. For example, a web browser might include "Internet" as a keyword even though it's not in the app's name, generic name, or description. As a result, a user searching for "Internet" will find the app. Here are some more examples:

* Files: **Folders;Browser;Explorer;Finder;Manager;**
* Terminal: **Command;Prompt;Cmd;Emulator;**
* System Settings: **Control;Panel;**

Keywords should be single words \(in [title case](./#title-case)\) separated by and terminated with a semicolon:

```text
Keywords=Foo;Bar;Baz;
```

See also: [Desktop Entry Specification](https://specifications.freedesktop.org/desktop-entry-spec/latest/index.html) from FreeDesktop.org
