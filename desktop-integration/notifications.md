---
description: Play sound and display bubbles to alert the user to certain important events
---

# Notifications

Notifications play a sound and are displayed as bubbles just below the system indicators. They briefly appear on screen where they can be selected to open the relevant app or manually dismissed by hitting the X icon. After a short time, they automatically slide away. Missed notifications can be seen in and cleared from the Notification Center indicator.

## Sounds

Notifications play a system sound by default, but app developers are able to set an appropriate app-specific sound for users to be able to more quickly recognize the source of the notification. Be sure to use the notifications API via LibNotify to set the sound so that it respects user settings and does not play a duplicate sound.

## Icons

By default, a notification will include the icon of the app that sent it. For certain apps, it might make sense to display a different relevant image along with a notification, like a user avatar if it's a communication app or album artwork if it's a music app.

## User Control

Keep in mind that users are in ultimate control over notifications and whether or not they appear. Being overly aggressive with your notifications is a quick way to get the user to turn them off entirely or even uninstall your app.

### Do Not Disturb

Users can enable Do Not Disturb mode from Notification Center or System Settings. Do Not Disturb blocks all notification bubbles and sounds until it is manually turned back off.

### Notification Settings

Notification bubbles, sounds, and appearance in Notification Center can each be toggled on or off on a per-app basis from the system notifications settings. Instead of including a global toggle for all notifications in your app, direct the user to the System Settings using a settings URL to open the Notifications page directly.

