---
description: Help users be faster and more confident
---

# Always Provide an Undo

Sometimes a user will perform an action which could possibly be destructive or traditionally irreversible. Rather than present the user with a warning, apps should let the user undo the action for an appropriate amount of time. Some prime examples of when this behavior is useful are:

* **Closing an app**. Rather than warning the user, automatically save their work and the app's state so they can return exactly where they left off. See [Closing](closing.md).
* **Deleting an item**. Instead of asking the user if they are sure, make the item "disappear" from the app, but provide an easy and intuitive way to undo the delete.
* **Sending an email**. Rather than asking the user if they want to send an email, let them undo or edit the message a short time after "sending."
* **Editing a photo**. Instead of asking the user if they want to destructively apply an edit, let them undo the edit and always keep the original backed up.

This behavior can be implemented by providing a buffer time between when the app shows the user what happened and actually performing the action, as long as the action is also actually performed if the user closes the window or otherwise navigates away. To keep the experience responsive, the app should always look as if it performed the action as soon as the user initiates it.

This behavior strikes the best balance of keeping out of the user's way while making sure they don't do something unintended. It's important to keep the undo action unobtrusive yet simple and intuitive; a common way of doing so is by using a toast or info bar, though other methods may also be appropriate.

Conventionally, the Ctrl+Z keyboard shortcut should also perform the undo action as long as undoing is possible or valid.

{% hint style="info" %}
See also: [Never Use a Warning When you Mean Undo](https://alistapart.com/article/neveruseawarning) by Aza Raskin
{% endhint %}

