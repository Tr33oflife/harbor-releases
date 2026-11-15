# Harbor — releases

This is the **releases-only** repo for the Harbor native Android app.

- Release APKs and their `version.json` files are published here, and
  nowhere else. The app's in-app updater reads this repo's latest
  release anonymously (no account, no token).
- **There is no source code in this repo.** Harbor's source lives
  elsewhere and is private; this repo exists only so the app can
  find its updates.

Each release carries:

- the signed APK, and
- `version.json` — `{"versionCode": N, "versionName": "X.Y.Z",
  "apk": "<asset name>", "sha256": "<apk sha256>"}` — which the app
  verifies (version-code comparison + SHA-256) before handing the
  download to the system installer.
