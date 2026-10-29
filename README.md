# Sipling Android updates

Signed Sipling Android APKs and the minimal update feed. The app's source code stays private.

- Update feed: https://ribhavjain22.github.io/sipling-android-updates/latest.json
- Installers live under `apks/`, named with their Android version code and SHA-256 (`sipling-<versionCode>-<sha256>.apk`).
- `latest.json` holds `versionCode`, `versionName`, `apkUrl`, `sha256` and `size` of the newest release.

Sipling checks the feed at most once a day. When a newer version is out, the Today screen offers it; the download is
checked against the feed's size and SHA-256 and against the installed app's package and signing key before Android's
installer is opened. Nothing installs silently. If Android asks to **Allow from this source**, allow it, return to
Sipling and tap **Install** again.

Published automatically by `tools/release/release-local.sh` in the Sipling repository (run by the owner's autopilot).
