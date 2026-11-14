# OpenUI

A clean, ad-free home screen for Fire TV and Android TV: your apps, Continue Watching, live scores, weather and a
Control Center, with no Amazon or Google ads.

This repository only holds the release APKs. OpenUI checks here for updates and shows a bell on Home when a new
version is out; press OK to install it.

## Install

1. On the TV, install **Downloader** from the app store.
2. Open it and enter:
   `github.com/sai-kondrakunta/openui-releases/releases/latest/download/openui.apk`
3. Allow Downloader to install apps when asked, then choose **Install**.
4. Open **OpenUI**, then Settings → **Phone setup** to sign in to Jellyfin and set things up from your phone.

Also install **OpenUI Guard** (`guard.apk` from the same release). It keeps Fire TV's own home screen hidden while
OpenUI updates. Downloader code: `github.com/sai-kondrakunta/openui-releases/releases/latest/download/guard.apk`

With a computer and `adb` (recommended): self-repair, Home without any Fire TV flash, Now Playing:

```
adb shell pm grant com.openui.launcher android.permission.WRITE_SECURE_SETTINGS
adb shell pm grant com.openui.launcher android.permission.READ_LOGS
adb shell pm grant com.openui.guard android.permission.READ_LOGS
```
