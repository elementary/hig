---
description: The primary method of discovering and using your app
---

# App Launcher

The primary method of discovering and using your app will be through an app launcher found in the Applications Menu or in the Dock. In order to provide these launchers you must install an appropriate .desktop file with your app. This includes giving your launcher an appropriate name, placing it in the correct category, assigning it an icon, etc.

.desktop files follow the freedesktop.org [Desktop Entry Specification](https://specifications.freedesktop.org/desktop-entry-spec/latest/index.html). They should be installed in `/usr/share/applications`.

The contents of .desktop files should follow this formula:

_**Name** is a\(n\) **GenericName** that helps you **Comment**._

```text
Name=Eddy
GenericName=Package Installer
Comment=Install Debian packages
Categories=System;PackageManager;
Keywords=Package;Apt;Dpkg;Install;
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

The following categories may be used to aid with searching or browsing for your app. Keep in mind that you can add more than one and you should add all that apply:

* AudioVideo
* Audio
* Video
* Development
* Education
* Game
* Graphics
* Network
* Office
* Science
* Settings
* System
* Utility

For more info, see the FreeDesktop.Org [menu entry](https://specifications.freedesktop.org/menu-spec/latest/apa.html) spec and the [list of additional categories](https://standards.freedesktop.org/menu-spec/latest/apas02.html)

Categories should be separated by and terminated with a semicolon:

```text
Categories=Graphics;Photography;Viewer;
```

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

