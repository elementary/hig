---
description: What the user sees the first time they use your app
---

# First Launch Experience

## Required Configuration

When a user first launches an app, they should be able to get down to business as quickly as possible. If configuration is not absolutely required for the first use, they should not be required to configure anything. If configuration is required, they should be presented with a clean and simple [welcome screen](./#welcome-screen) within the app. Avoid separate configuration dialogs when launching.

## Speed of Launch

Your app's first launch is the user's first impression of your app; it's a chance to really show off its design and speed. If your app has to configure things in the background before visibly launching, it gives the user the impression that the app is slow or will take a long time to start up. Instead, focus on making the application window appear fast and ready to be used, then do any background tasks behind the scenes. If the background task is blocking \(e.g. the user is unable to perform certain tasks until it's complete\), show some type of indication that a background process is happening and make the blocked user interface items insensitive \(see: [Widget Concepts](./#widget-concepts)\).

## Welcoming the User

If there is no content to show the user, provide actions they can act upon by using a simple [welcome screen](./#welcome-screen). Let them open a document, add an account, import a CD, or whatever makes sense in the context of the app.

## Resetting the App

If a user explicitly "resets" the app \(ex. by deleting all songs in a music library or removing all mail accounts in a mail client\), it should return to its first-launch state.

