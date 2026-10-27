# GameTime MN TV — box releases

Release feed for the GameTime MN TV app on the Android TV boxes. Each
release (tag `tvbox-v<versionCode>`) has two files:

- `GameTimeMN-TV-tvbox-<versionCode>.apk` — the signed app
- `update.json` — `{ "versionCode", "url", "sha256" }`, read by the boxes at
  `releases/latest/download/update.json`

Boxes only install an update whose SHA-256 matches `update.json`, and Android
only accepts it if it's signed with the same key as the installed app.

Releases are created by `scripts/publish-tvbox-update.sh` in the app's
source repository. Don't edit or delete releases by hand: the newest release
is what every box installs.
