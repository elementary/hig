---
description: What happens when closing your app
---

# Closing

When a user closes an app, it's typically because they're done using it for now and they want to get it out of the way.

## Saving State

Apps should save their current state when closed so they can be reopened right to where the user left off. Typically, closing and reopening an app should be indistinguishable from the legacy concept of minimizing and unminimizing an app; that is, all elements should be saved including open documents, scroll position, undo history, etc.

Because of the strong convention of saved state, elementary OS does not expose or optimize for legacy minimize behavior; e.g. there is no minimize button, and the Multitasking View does not distinguish minimized windows.

## Closing the App Window

Apps should never minimize instead of closing, as that puts the app window into a state that is foreign to users of elementary OS. Instead, windows should close or hide and re-open with a [saved state](./#saving-state). Any ongoing or [background tasks](./#background-tasks) should be completed soon after the window is closed, then the app should quit so as to not use unnecessary resources.

