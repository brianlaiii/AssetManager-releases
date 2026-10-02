# Asset Manager

A Maya tool for browsing, publishing, and reusing versioned assets.

## Download

Download the installation ZIP from [GitHub Releases](https://github.com/brianlaiii/AssetManager-releases/releases/latest).
The application includes its Python source under the MIT License.

Use the named installation ZIP. GitHub's automatic Source code archives contain this release page and license.

## Compatibility

The initial macOS release supports Maya 2024, 2026, and 2027.
It uses Maya's included Python and Qt libraries. Maya must be installed separately.
Geometry checks use their Python implementations. Native acceleration modules are not bundled.

## Install

1. Download and extract the installation ZIP.
2. Close Maya before replacing an existing installation.
3. Copy the extracted `asset_manager` folder into your Maya user scripts folder.
4. Start Maya and run this in the Python Script Editor:

```python
import asset_manager
asset_manager.launch()
```

To find your Maya user scripts folder, run:

```python
import maya.cmds as cmds
print(cmds.internalVar(userScriptDir=True))
```

## Updates

Open **Settings > Updates** or **Help > Check for Updates**.

- Checks can run automatically when Asset Manager opens.
- A new version shows its release notes before installation.
- Click **Update** to download and prepare a compatible package.
- Restart Maya to use the new version.
- The previous version is retained. Your settings and project assets are kept separate.

Update checks read public GitHub release information. They require no GitHub login.
The updater does not send user names, settings, workspace paths, or asset files.

## Support

Report issues through this repository's Issues page. Include the application version, Maya version, and a short description.

## License

MIT. See [LICENSE](LICENSE).
