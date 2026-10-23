# Release Notes

## 0.1.5

- Improved Media Player close handling and added **File > Close** as another way to close the player.
- Escape and other close paths now share annotation confirmation and cleanup. Save, Discard, and Cancel protect unsaved annotations, including text still being edited. Escape inside the text editor continues to cancel that edit.
- Closing stops playback and cache timers. Delayed frame and gamma work cannot restart a closed player's caches.
- Closing during an MP4 export stops the export, releases its temporary files after the process exits, and avoids a completion popup for the closed player.
- Added Windows native close-command handling while retaining the normal tool window.
- Problem reports now distinguish observed Windows close-button input, native close commands, dialog close requests, annotation cancellation, and cleanup stages.

Download the ZIP for your computer:

- [Download for Mac](https://github.com/brianlaiii/AssetManager-releases/releases/download/v0.1.5/asset-manager-0.1.5-macos.zip)
- [Download for Windows](https://github.com/brianlaiii/AssetManager-releases/releases/download/v0.1.5/asset-manager-0.1.5-windows.zip)
- [Installation guide](https://github.com/brianlaiii/AssetManager-releases#install-on-windows)

Player close checks pass with the Mac Maya 2024, 2026, and 2027 Qt runtimes. Actual File > Close, titlebar close, Escape, annotation Cancel/Discard, and continued main-window use were checked in Mac Maya 2024.
Automated CI was unavailable for this release. Native Windows package and updater checks have not been run for this version.
The original Windows titlebar X failure has not been reproduced or verified as fixed on Windows Maya. The Windows Maya interface, asset operations, and rendering remain untested in Maya.

## 0.1.4

- Added Settings > Problem Reports and Help > Report a Problem.
- Describe a problem, preview the report, and export one ZIP to send privately to the person helping you. No account or automatic upload is required.
- Reports include app, Maya, Qt, and system versions, recent retained Asset Manager actions, and observed errors.
- Common credentials, email addresses, and absolute paths are filtered. Review the text before sharing. Scene files, textures, settings files, and screenshots are not attached.
- Activity logs stay local and have a size limit. Recording starts when this version opens; older actions cannot be recovered.
- Added Media Player close diagnostics to help investigate failures. This release does not claim to fix the reported Windows player close issue.
- Settings scrolls to keep the report panel reachable in smaller windows.

Download the ZIP for your computer:

- [Download for Mac](https://github.com/brianlaiii/AssetManager-releases/releases/download/v0.1.4/asset-manager-0.1.4-macos.zip)
- [Download for Windows](https://github.com/brianlaiii/AssetManager-releases/releases/download/v0.1.4/asset-manager-0.1.4-windows.zip)
- [Installation guide](https://github.com/brianlaiii/AssetManager-releases#install-on-windows)

The report flow has been checked in Mac Maya 2024 and with Qt5 and Qt6 runtimes.
Automated CI was unavailable for this release. Native Windows package, diagnostics, and updater checks were not run for this version.
The Windows Maya interface, asset operations, and rendering have not yet been tested in Maya.

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
