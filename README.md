# Realmfarers Releases

Prebuilt releases of **Realmfarers (千界旅团)**, a 3D top-down action RPG. This repository only contains the build workflow; the game source is not published here.

## Download

Go to [Releases](../../releases), pick a version and download the zip for your platform:

- `Realmfarers-<version>-windows.zip`: unzip and run `Realmfarers.exe`.
- `Realmfarers-<version>-linux.zip`: unzip and run `./Realmfarers.x86_64` (`chmod +x` it if needed).
- `Realmfarers-<version>-macos.zip`: unzip and open `Realmfarers.app` (universal: Apple Silicon and Intel).

Dev (prerelease) builds are named `Realmfarers-Dev-<version>-<platform>.zip` and contain `Realmfarers Dev.exe`, `Realmfarers-Dev.x86_64` or `Realmfarers Dev.app`. They keep their own settings and updates, separate from the stable game.

The game checks this repository's releases on startup and downloads small content updates (`*.pck`, described by `manifest.json`) automatically; they apply on the next launch. When an update needs a newer engine, the game asks you to download the full zip instead.

Tags ending in `-dev` are development builds (pre-releases); plain `v<version>` tags are stable.

## First launch notes

**macOS**: the app is ad-hoc signed, not notarized, so Gatekeeper blocks it the first time. Right-click (or Control-click) `Realmfarers.app` and choose **Open**, then confirm. On newer macOS versions you may instead need to go to **System Settings → Privacy & Security** and click **Open Anyway**. If macOS says the app is "damaged", run `xattr -dr com.apple.quarantine Realmfarers.app`.

**Windows**: the exe is unsigned, so SmartScreen may show "Windows protected your PC". Click **More info → Run anyway**.
