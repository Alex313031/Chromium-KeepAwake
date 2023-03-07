# Chromium Keep Awake <img src="https://raw.githubusercontent.com/Alex313031/Chromium-KeepAwake/main/logo.png" width="64">

Chromium/Chrome extension to override system power-saving settings.

 - This is a fork of https://chrome.google.com/webstore/detail/keep-awake/bijihlabcfdnabacffofojgmehjdielb, except:
 > - It was updated to [Manifest Version 3](https://developer.chrome.com/docs/extensions/mv3/intro/).  
 > - Updated the [manifest.json file](https://github.com/Alex313031/Chromium-KeepAwake/blob/main/src/manifest.json) with more values.  
 > - Added more [icon](https://github.com/Alex313031/Chromium-KeepAwake/tree/main/src/img) image sizes.  

----------------------------------------------------------

This extension makes it easy to temporarily disable power management on Chrome OS.

It adds an icon in the upper-right corner of the browser that can be clicked to switch between modes where the screen is kept on (sun icon), the system is prevented from sleeping (sunset), or power-saving settings are left unchanged (moon).

----------------------------------------------------------

Frequently-asked questions:

* Will this extension prevent a Chromebook from suspending when its lid is closed?

No, but if an external display is connected, recent versions of Chrome OS will remain awake when the lid is closed.

* What's the difference between the "screen is kept on" and "system is prevented from sleeping" modes?

When the system is prevented from sleeping (sunset icon), network connections will remain active; this may be useful if using e.g. the Secure Shell app. The screen will still dim and turn off eventually, though. In the "screen is kept on" mode (sun icon), the system will avoid sleeping and the display will additionally remain on.

* What do the icons mean?

The sun icon means that the screen will be kept on. The moon icon means that the system will behave the same way that it would if the extension were not installed. The sunset icon is a middle ground: the system will avoid sleeping (as described above) but the screen will still turn off.

----

Release notes for version 1.9.1 (1.9.0 was never published):

It was updated to [Manifest Version 3](https://developer.chrome.com/docs/extensions/mv3/intro/).

Updated the manifest.json file with more values.

Added more icon image sizes.

Release notes for version 1.8 (1.7 was never published):

Removed windows.onCreated hack added to work around http://crbug.com/222473 on Chrome OS.

Release notes for version 1.6:

Removed scary "tabs" permission.  (Technical details: There's a bug where Chrome doesn't notify extensions after the user logs in on Chrome OS.  This extension loads its saved state whenever a window is created instead.  The chrome.windows API is documented as requiring the "tabs" permission but listening for window creation appears to work without it.)

Release notes for version 1.5:

This version fixes a bug where the previous mode would not be correctly restored after logging out and back in.

Note also that only the "keep the screen on" and "unchanged" modes are available in Chrome 26.  In Chrome 27, the "prevent the system from sleeping" mode is also available.
