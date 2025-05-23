# Web Browser Extended

## Description

This a fork of the official "Web Browser" plasmoid shipped with KDE Plasma 6. It supports more features than the official plasmoid. Only KDE Plasma 6 supported.

Bug reports and pull requests are welcomed.

## Features

- All features included in the official "Web Browser" plasmoid

- **An option to use a persistent browser profile stored on disk** (default off). The name of the profile can be configured.

  The official "Web Browser" applet use the "off the record" profile, which stores all browser data in memory. That means all login data are gone after reboot. This option fixes that and keeps all login data on disk.

  The browser profiles created by this applet are not shared with regular web browser applications. If you are using multiple instances of this applet, **use different browser profiles for each instance**, or otherwise your cookies could be corrupted.

  Currently, a browser profile directory is located at `~/.local/share/plasmashell/QtWebEngine/<profile_name>`. It will **not** be deleted when not needed anymore (there is no way to delete a directory using only QML). You need to clean the abandoned profiles manually if you change the profile name or remove an instance of this applet.

- **Optional web engine settings**, include:

  - **Allow JavaScript on the web page to access system clipboard** (default off). Note that unrestricted clipboard access is a potential security concern, so use this option with care.

  - **Force all web pages to render in a dark theme** (default off). This option is equivalent to `chrome://flags/#enable-force-dark` in Chromium. Even if the web page does not support dark mode, this option will force a dark theme onto it.

  - **Allow web pages to display HTML5 notification** (default off). This option grants notification permissions to all web pages. It also allows push service via  [Firebase Cloud Messaging (FCM)](https://firebase.google.com), a Google service.

  - **Allow web pages to capture media from microphone and camera** (default off).

  - **Allow web pages to capture user screen and application audio** (default off).

  - **An option to inject custom JavaScript code into web pages** (default off). The code is executed after the web page has finished loading.

- **Transparent background** (default off). This option is configurable in edit mode.

## Installation

Download the latest release `web-browser-extended.plasmoid`. Run `kpackagetool6 --type Plasma/Applet --install web-browser-extended.plasmoid` to install the applet.
