# Providing Feedback

There are several ways to provide feedback in elementary OS, depending on the nature and severity of that feedback.

* **Toasts** affirm user action and can provide a contextual action, such as "Undo" and dismiss automatically after a short timeout.
* **Info Bars** provide basic information and can provide a contextual action. They do not obscure other content and are not dismissed automatically.
* **Message Dialogs** can be used to provide extensive information and offer multiple possible actions. They can be used when immediate action is required.
* **Notifications** provide basic information and can be shown whether or not your app is focused. They are usually dismissed automatically and can be reviewed later in the notifications indicator.
* **Badges and Progress Bars** overlay your app's icon in the operating system and convey the status of long running actions whether or not your app is focused.

## Toasts

Toasts are ephemeral in-app notifications overlaid on top of other content used to affirm user action and/or provide a time-sensitive contextual action. After a short timeout, a toast is automatically dismissed. Because they are ephemeral, toasts should follow recent user action when the user is expected to engaging with the app. A toast can offer a contextual action that can be triggered as long as the toast is visible. A toast includes a manual dismiss button, e.g. if it is likely to be covering content the user may be more interested in.

A toast's title should be phrased to affirm user action, even when providing an [undo](../user-workflow/always-provide-an-undo.md) action. For example, "Foo was deleted", while offering an action to "Undo".

Use a toast to affirm user action and provide a contextual action, like confirming content was deleted while offering an undo, or informing the user that an in-app process completed while offering a button to navigate to the result of the process. If you provide a toast in your app to notify of the result of a background process, consider only using a toast if your app window is focused while throwing a system notification if the window is not focused.

## Info Bars

Info bars provide contextual information and actions to the user with varying levels of severity.

![Infobars](https://elementary.io/images/docs/human-interface-guidelines/infobars/infobars.png)

It is important to determine the severity or type of info bar to use. There are four types of info bars available:

* **Information**: Supplemental information and an optional action the user may perform. Shows as white in the UI.
* **Question**: A non-critical question for the user. An answer of some sort is expected, but it's not urgent or severe. Shows as blue in the UI.
* **Warning**: Lets the user know something unexpected or bad may happen and provides an action to resolve it. Displays as yellow in the UI.
* **Error**: Informs the user of an error that has occurred and requires a user action to resolve it. Reserved for critical situations. Displays as red in the UI.

## Message Dialogs

A message dialog contains both primary and secondary text as well as clearly labeled buttons.

The primary text contains a brief summary of the situation and offers a suggested action. Primary text should be in [sentence case](container-widgets.md#sentence-case) and not include [terminating punctuation](container-widgets.md#terminating-punctuation), except in the case of questions.

The secondary text provides a more detailed description of the situation and describes any possible side effects of the available actions. It's important to note that a user should only need the primary text to make a decision and should only need to refer to the secondary text for clarification. Secondary text should be in [sentence case](container-widgets.md#sentence-case) with [terminating punctuation](container-widgets.md#terminating-punctuation).

{% hint style="info" %}
[`Granite.MessageDialog`](https://valadoc.org/granite/Granite.MessageDialog.html) is the prefered way to create message dialogs with the correct layout
{% endhint %}

### Button Order

![Button Order](https://elementary.io/images/docs/human-interface-guidelines/dialogs/button-order.png)

* All dialogs should contain an affirmative button that performs the action suggested in the primary text. This button should be aligned to the very end of the dialog.
* For dialogs that are displayed in response to user action \(such as "Quit"\), provide a "Cancel" button directly before the affirmative button.
* If your dialog has alternative actions, list them before the "Cancel" button.
* If your dialog has incidental actions \(actions that do not close the dialog such as "Help"\), these should be aligned to the start of the dialog.

### "OK" is not Okay

When presenting a dialog to a user, always use explicit action names like "Save..." or "Shut Down". Consider how "OK" lets users proceed without understanding the action they are authorizing. Not all users will read the question or information presented to them in a dialog. Using specific action names will make it harder for a user to select an unintended action and may even encourage them to read the presented information before making a selection.

### Suggested and Destructive Actions

If the primary action is not destructive, its button should be given the `.suggested-action` style class, rendering it in a highlighted style by default. It should usually be focused by default so it's quicker for the user to perform the action using the keyboard.

If the primary action is destructive—i.e. it cannot be easily reversed or undone—it should be given the `.destructive-action` style class, rendering it in a red style by default. Destructive actions should not be focused by default to prevent accidental activation.

Multiple suggested and/or destructive actions should not co-exist in the same context; there should only be one of either type in a dialog.

## Notifications

Notifications play a sound and are displayed as bubbles just below the system indicators. They briefly appear on screen where they can be selected to open the relevant app or manually dismissed by hitting the X icon. After a short time, they automatically slide away. Missed notifications can be seen in and cleared from the Notification Center indicator.

### Sounds

Notifications play a system sound by default, but app developers are able to set an appropriate app-specific sound for users to be able to more quickly recognize the source of the notification. Be sure to use the notifications API via LibNotify to set the sound so that it respects user settings and does not play a duplicate sound.

### Icons

By default, a notification will include the icon of the app that sent it. For certain apps, it might make sense to display a different relevant image along with a notification, like a user avatar if it's a communication app or album artwork if it's a music app.

### User Control

Keep in mind that users are in ultimate control over notifications and whether or not they appear. Being overly aggressive with your notifications is a quick way to get the user to turn them off entirely or even uninstall your app.

#### Do Not Disturb

Users can enable Do Not Disturb mode from Notification Center or System Settings. Do Not Disturb blocks all notification bubbles and sounds until it is manually turned back off.

#### Notification Settings

Notification bubbles, sounds, and appearance in Notification Center can each be toggled on or off on a per-app basis from the system notifications settings. Instead of including a global toggle for all notifications in your app, direct the user to the System Settings using a settings URL to open the Notifications page directly.

## Dock Integration

![Dock](https://elementary.io/images/docs/human-interface-guidelines/dock-integration/dock.svg)

### Progress Bars

Make progress bars unambiguous by referring to a single, specific task. For example, use progress bars to indicate the status of lengthy processes like file transfers and encoding. Do not use progress bars to compound the progress of different types of action.

* **Good Example**: Installation progress in AppCenter
* **Bad Example**: Combined progress of downloading an album, burning a CD, and syncing a mobile device in a music app

### Badges

A badge shows a count of actionable items managed by your app. Its purpose is to inform the user that there are items that require user attention or action without being obtrusive. This is a passive notification. A badge should not show totals or rarely changing counters. If the badge is not easily dismissed when the user views your app, it is likely that this is not a good use of a badge.

* **Good Example**: Unread messages in a mail app
* **Bad Example**: Total number of photos in a photo library
