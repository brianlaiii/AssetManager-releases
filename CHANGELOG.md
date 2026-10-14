# Release Notes

## 0.1.3

- Publish saves native Maya geometry without rerunning validation checks.
- Missing map1 and non-manifold geometry no longer block item, pack, or cache geometry saves.
- Alembic caches, proxies, previews, and geometry sidecars are optional. Full import can use the saved Maya geometry when these extras fail.
- Added a separate map1 check and Fix. The Fix preserves existing UV sets.
- Browse, search, and Manage ignore folders whose names start with an underscore or dot.
- Includes Settings > Updates and Help > Check for Updates. Public installations receive compatible stable releases from this repository after a Maya restart.
- Arnold media keeps raw ACEScg EXRs separately from JPEG previews and preserves incomplete jobs for retry. JPEG previews require an optional configured Python runtime.
- One release with installation ZIPs for Mac and Windows. Copy the complete asset_manager folder into the shared Maya scripts folder.

Download the ZIP for your computer:

- [Download for Mac](https://github.com/brianlaiii/AssetManager-releases/releases/download/v0.1.3/asset-manager-0.1.3-macos.zip)
- [Download for Windows](https://github.com/brianlaiii/AssetManager-releases/releases/download/v0.1.3/asset-manager-0.1.3-windows.zip)
- [Installation guide](https://github.com/brianlaiii/AssetManager-releases#install-on-windows)

Mac Maya operation checks are run before publication. Windows package and updater checks are run on Windows before publication.
The Windows Maya interface, asset operations, and rendering have not yet been tested in Maya.

## 0.1.2

- One release with installation ZIPs for Mac and Windows.
- Mac: Maya 2024, 2026, and 2027. Windows: Maya 2024, 2025, 2026, and 2027.
- Browse, publish, and reuse versioned Maya assets.
- Check for updates in Settings or Help. Install updates after restarting Maya.
- Keep local settings, project assets, and the previous installation separate.
- Includes the MIT License and simple installation steps for artists.

Download the ZIP for your computer:

- [Download for Mac](https://github.com/brianlaiii/AssetManager-releases/releases/download/v0.1.2/asset-manager-0.1.2-macos.zip)
- [Download for Windows](https://github.com/brianlaiii/AssetManager-releases/releases/download/v0.1.2/asset-manager-0.1.2-windows.zip)
- [Installation guide](https://github.com/brianlaiii/AssetManager-releases#install-on-windows)

Mac has been tested in Maya. Windows package and updater checks have passed.
The Windows Maya interface, asset operations, and rendering have not yet been tested in Maya.
