# Web Browser Extended

## Description

This a fork of the official "Web Browser" plasmoid shipped with KDE Plasma 6. It supports more features than the official plasmoid. Only KDE Plasma 6 supported.

Bug reports and pull requests are welcomed.

## Features

- All features included in the official "Web Browser" plasmoid

- **An option to use a persistent browser profile stored on disk** (default off). The name of the profile can be configured.

  The official "Web Browser" applet use the "off the record" profile, which stores all browser data in memory. That means all login data are gone after reboot. This option fixes that and keeps all login data on disk.

  The browser profiles created by this applet are not shared with regular web browser applications. However, multiple instances of this applet with the same profile name share the same browser profile.

  Currently, a browser profile directory is located at `~/.local/share/plasmashell/QtWebEngine/<profile_name>`. It will **not** be deleted when not needed anymore (there is no way to delete a directory using only QML). You need to clean the abandoned profiles manually if you change the profile name or remove an instance of this applet.

## Installation

Download the latest release `web-browser-extended.plasmoid`. Run `kpackagetool6 --type Plasma/Applet --install web-browser-extended.plasmoid` to install the applet.
