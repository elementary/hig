# Toast

Toasts are ephemeral in-app notifications overlaid on top of other content used to affirm user action and/or provide a time-sensitive contextual action. After a short timeout, a toast is automatically dismissed. Because they are ephemeral, toasts should follow recent user action when the user is expected to engaging with the app. A toast can offer a contextual action that can be triggered as long as the toast is visible. A toast includes a manual dismiss button, e.g. if it is likely to be covering content the user may be more interested in.

A toast's title should be phrased to affirm user action, even when providing an [undo](../../human-interface-guidelines/user-workflow/always-provide-an-undo.md) action. For example, "Foo was deleted", while offering an action to "Undo".

Use a toast to affirm user action and provide a contextual action, like confirming content was deleted while offering an undo, or informing the user that an in-app process completed while offering a button to navigate to the result of the process. If you provide a toast in your app to notify of the result of a background process, consider only using a toast if your app window is focused while throwing a system notification if the window is not focused.

