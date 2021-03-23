# Background Tasks

If it makes sense to continue a process in the background \(such as downloading/transferring, playing music, or executing a terminal command\) the app back-end should continue with the task and close when the task is finished. If it's not immediately apparent that the process has completed \(as with the file download/transfer or terminal command\), the app may show a notification informing the user that the process has completed. If it is apparent, as with the music, no notification is necessary.

If an app performs repeat background tasks \(such as a mail client fetching mail\), the background tasks should be completed by a daemon and not rely on any window being open.

## Re-Opening the App Window

If the user re-opens an app while a background process is still executing, the app should be exactly where it would be if the window had been open the whole time. For example, the terminal should show any terminal output, the music player should be on the same page it was when closed, and the browser should come back to the page it was on previously. For more details, see the discussion of app state on a [Normal Launch](./#normal-launch).

{% hint style="info" %}
See also: [That's It, We're Quitting](https://blog.ubuntu.com/2011/03/07/quit) by Matthew Paul Thomas
{% endhint %}

