# Accessible Configuration

Providing settings can be a way to make sure an app is accessible to a wider set of users with special needs, but it can also be an easy way out of making design decisions about an app's behavior. Just like with problems of feature bloat, settings mean more code, more bugs, more testing, more documentation, and more complexity. When considering adding options to your app, try to strike a balance of making your app more accessible without pushing design work onto your users.

## Build for the “Out of the Box” Experience

Design with sane defaults in mind. elementary OS apps put strong emphasis on the out of the box experience. If your app has to be configured before a user is comfortable using it, they may not take the time to configure it at all and simply use another app instead.

## Ask the Operating System

Get as much information automatically as possible. Instead of asking a user for their name or their location, ask the system for this information. This cuts down on the amount of things a user has to do and makes your app feel more intelligent and integrated.

## Is It Really About Accessibility?

Ask yourself if the configuration option you are adding is really necessary to make your app more accessible or if it makes sense to have a user make this decision. Don't ever ask users to make uninformed engineering or design decisions.

## When You Absolutely Have To

Keep things contextual. Instead of tucking away preferences in a configuration dialog, think about displaying them in context with the objects they affect \(much like how shuffle and repeat options appear near your music library\).

If your app needs to be configured before it can be used \(like a mail client\), present this configuration inside the main window much like a [Welcome Screen](../../widgets/ui-toolkit-elements/#welcome-screen). Once again, make sure this is really necessary set-up. Adding unnecessary configuration screens stops users from doing what they wanted to do when they opened your app in the first place.

{% hint style="info" %}
See also:

1. [Checkboxes That Kill Your Product](https://limi.net/checkboxes) by Alex Limi
2. [Don't Give Your Users Shit Work](https://zachholman.com/posts/shit-work/) by Zach Holman
3. [The Wizard Anti-Pattern](http://stef.thewalter.net/installer-anti-pattern.html) by Stef Walter
{% endhint %}

