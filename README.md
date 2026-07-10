# EpicZ-Updates

Static update feed for the [EpicZ](https://github.com/iamvdk09) kiosk music
player. The app polls `update.json` on the `main` branch (via
`raw.githubusercontent.com`) to check for new releases.

## Files

- `update.json` — metadata the app reads: version info, APK URL, SHA-256, size, release notes.
- `app-release.apk` — the APK the app downloads when an update is available.
- `release-notes.md` — human-readable changelog (not read by the app itself).

## Publishing a new release

1. In the EpicZ project, bump `versionCode` and `versionName` in `app/build.gradle.kts`, then build the release/debug APK.
2. Compute its checksum: `sha256sum app-release.apk` (or `certutil -hashfile app-release.apk SHA256` on Windows).
3. Replace `app-release.apk` in this repo with the new build.
4. Update `update.json`:
   - `versionName` / `versionCode` — must match the new build exactly.
   - `apkUrl` — leave as-is unless the filename changes.
   - `sha256` — the checksum from step 2.
   - `size` — the new file's byte size.
   - `releaseNotes` — short bullet list shown in the app.
5. Update `release-notes.md` for the record.
6. Commit and push to `main`.

That's it — no changes to the EpicZ app code are needed for a release. The
next time a device taps **Check for Updates**, it will see the new
`versionCode` and offer the download.
