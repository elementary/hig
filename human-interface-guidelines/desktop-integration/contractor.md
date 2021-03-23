---
description: Share files and data with other apps
---

# Contractor

Contractor is a service and a protocol for exposing services easily between apps. It lets apps interact with other apps and services without hard-coded support for them. You simply add [Contractor](https://github.com/elementary/contractor) support, and then any service registered with Contractor is now available for your app to use. Your app can integrate with Contractor in two different ways:

* Register one of its functions as a service that can be used from other apps
* Implement the contractor menu or otherwise access contractor to receive a list of services that can handle the data your app manages

## Displaying Results from Contractor

Contractor results are typically presented to users in menu form. Keep the following in mind when presenting Contractor results:

* If the item acted upon is one of many items visible, such as in an icon view, be sure to display results in a way that is directly related to the item such as in a context menu.
* If the item acted upon is the only item currently visible, such as a web page or a contact in Dexter, contractor can be displayed in a toolbar menu.
* Never display the target app's name. The menu string is the intended display name for that app. Doing so can lead to redundant messages such as, "Set image as wallpaper \(wallpaper\)" and it is always irrelevant to a user's needs.

