---
description: When it is or isn't appropriate to use
---

# System Indicators

Indicators are small icons that live on the top panel. They give users a place to glance for quick information about the state of the system. Selecting an icon opens a small contextual menu with related actions available to the user, including a way to get the the full related system settings.

![Indicators](https://elementary.io/images/docs/human-interface-guidelines/system-indicators/panel.svg)

## Does Your App Need an Indicator?

Indicators are designed for the system; they display information that is relevant to or affects the general usage of the device. Given that users will probably install many third-party apps, we must be careful about the number of indicators we show and how they behave. Keep in mind that only a very small set of applications need or benefit from an indicator.

**Avoid adding an indicator** if:

* **It will only appear while your app's main window is open.** LibUnity already provides a great API for showing application statuses on your app's icon in the dock. Only use an indicator if it will show while your app's main window is closed.
* **You want a persistent/smaller launcher.** Launchers are already stored in the dock in a way that gives the user control over persistence and size. The indicator area should never be used for an app launcher. If you want to add special actions to your launcher, Quicklists should be used, not an indicator.
* **Your app is for IM, IRC, e-mail, news-reading, or music playback.** Instead, integrate the application with the dock, notifications, or the existing sound menu.
* **You want to show the user your app is running.** Users expect that apps will run in the background when it makes sense. To inform the user of events while your app is running in the background, use notifications.
* **It does not show system-wide information.** App-specific information should be exposed using the dock and/or notifications.

{% hint style="info" %}
See also:

1. [Developer Tips: Backgrounding & System Integration](https://medium.com/elementaryos/developer-tips-backgrounding-system-integration-31c1f7226606) by Cassidy James Blaede
2. [Farewell to the Notification Area](https://blog.ubuntu.com/2010/04/21/notification-area) by Matthew Paul Thomas
3. [Status Icons and GNOME](https://blogs.gnome.org/aday/2017/08/31/status-icons-and-gnome/) by Allan Day
{% endhint %}

