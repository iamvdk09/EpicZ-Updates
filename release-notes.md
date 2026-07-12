# EpicZ Release Notes

## 1.3.2 (versionCode 7)

- Home screen redesign: Favorites now appears first, followed by a compact
  2x3 grid of your 6 most recent songs, then Playlists.
- Recent Songs updates automatically as you keep listening, and stays capped
  at 6 so it no longer crowds out the rest of Home.

## 1.3.1 (versionCode 6)

- **IMPORTANT:** this build's internal package identity changed, so it
  installs as a separate app instead of upgrading in place. After
  installing, manually uninstall the old EpicZ app once — every update
  after this one will apply in place again as usual.
- Removed the kiosk-mode status card from Settings.

## 1.3.0 (versionCode 5)

- New: Search now has an "Online Results" section — search and stream music
  from Jamendo's online catalog alongside your local library.
- Online tracks stream instantly with no download required, and work with
  Play Next, Add to Queue, Favorites, and Playlists just like local songs.
- Automatically falls back to local-only results when there's no internet
  connection.

## 1.2.1 (versionCode 4)

- Fixed a bug where Settings kept showing "Install Update" even after an
  update had already been successfully installed.
- The app now revalidates its cached update state against the running
  version every time Settings or Software Updates opens, and clears out any
  stale downloaded APK left behind by a previous install.

## 1.2 (versionCode 3)

- Every song list in the app (Home, Albums, Artists, Library, Favorites,
  Playlists, Search) now has a consistent ⋮ overflow menu: Play Next, Add to
  Queue, Add to Playlist, Delete Song.
- Long-press any song to add it to a playlist from a bottom sheet, including
  creating a new playlist on the spot.
- Library has a new Refresh button (next to Search) to pick up newly added
  or deleted songs immediately, without restarting the app.
- Library tabs reordered to Albums, Songs, Artists — Songs still opens by
  default.

## 1.1 (versionCode 2)

- Now Playing's volume icon toggles mute: tap once to mute, tap again to
  restore the volume you were at before muting.
- Rebuilt and signed with EpicZ's release key (previous builds were
  debug-signed). Anyone on an older debug-signed install will need to
  uninstall and reinstall once to pick this up; all updates after this one
  will apply in place.

## 1.0 (versionCode 1)

- Self-hosted OTA update system: EpicZ can now check this repository for new
  versions, download them with resumable/verified transfers, and install
  them directly from the device — no Play Store required.
- Queue screen now shows only the current track and what's coming up next.
- Songs list gained a context menu: Play Next, Add to Queue, and Delete Song.
