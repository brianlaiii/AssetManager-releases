# Asset Manager

A Maya tool for browsing, publishing, and reusing versioned assets.

## Download

Click the ZIP download for your computer:

| Your computer | Download | Maya versions |
| --- | --- | --- |
| Mac | [Download for Mac (.zip)](https://github.com/brianlaiii/AssetManager-releases/releases/download/v0.1.1/asset-manager-0.1.1-macos.zip) | 2024, 2026, 2027 |
| Windows | [Download for Windows (.zip)](https://github.com/brianlaiii/AssetManager-releases/releases/download/v0.1.2-beta.1/asset-manager-0.1.2-beta.1-windows.zip) | Test targets: 2024, 2025, 2026, 2027 |

The ZIP is ready to use in Maya. You do not need GitHub login, Git, a separate Python installation, or a build step.
Both links download the ready-to-install ZIP directly.

Windows is currently a test version. Its Maya interface, asset operations, and renderer behavior still need testing in Windows Maya.
Try it in a temporary project first. The stable Mac download remains available.

## Install on Windows

1. Close **all** Maya windows.
2. Right-click the downloaded ZIP and choose **Extract All**. Open the extracted folder. You should see a folder named `asset_manager`.
3. Open **File Explorer**. Click **Documents**, then open **maya**.
4. Open **scripts**. If it is missing, create a folder named `scripts`.
5. Copy the whole `asset_manager` folder into **scripts**.

The folder should now be here:

```text
Documents/maya/scripts/asset_manager
```

Use the **scripts** folder directly inside **maya**. Keep it outside the `2024`, `2025`, `2026`, and `2027` folders.
This shared location lets your supported Maya versions use the same installation.
Use **Documents** from File Explorer's sidebar, including when it is stored in OneDrive.

If `asset_manager` is already there, move the old folder somewhere safe before copying the new one.
Copy the folder itself, with everything inside it.

## Install on Mac

1. Close **all** Maya windows.
2. Double-click the downloaded ZIP. Open the extracted folder. You should see a folder named `asset_manager`.
3. Open **Finder**. In the top menu, choose **Go > Go to Folder**.
4. Copy this location into the box, then press **Return**:

```text
~/Library/Preferences/Autodesk/maya/
```

5. Open **scripts**. If it is missing, choose **File > New Folder** and name it `scripts`.
6. Copy the whole `asset_manager` folder into **scripts**.

The folder should now be here:

```text
~/Library/Preferences/Autodesk/maya/scripts/asset_manager
```

Use this shared **scripts** folder. Keep it outside the Maya year folders.
Your supported Maya versions can use the same installation.
If `asset_manager` is already there, move the old folder somewhere safe before copying the new one.

## Open Asset Manager in Maya

These steps are the same on Mac and Windows.

1. Start Maya.
2. In Maya's top menu, choose **Windows > General Editors > Script Editor**.
3. In the lower area, click the **Python** tab.
4. Copy and paste these two lines into that lower area:

```python
import asset_manager
asset_manager.launch()
```

5. In the Script Editor menu, choose **Command > Execute**. Asset Manager opens.

You only need to copy these lines. You do not need to write any code.

To add a button for next time, select both lines and choose **File > Save Script to Shelf** in the Script Editor.
Name the button **Asset Manager** and choose **Python** if asked.
Click that shelf button whenever you want to open the tool. Create it once in each Maya version you use.

## If the tool does not open

- Restart Maya after copying the folder.
- Check that `asset_manager` is directly inside **scripts**. Avoid `scripts/asset_manager/asset_manager`.
- Make sure the Script Editor tab says **Python**.
- Use a Maya version listed in the download table above.
- If your studio uses a custom Maya folder, ask your pipeline team where to put shared scripts.

## Updates

Open **Settings > Updates** or **Help > Check for Updates**.

1. Click **Check for Updates**.
2. If a compatible stable version is available, click **Update**.
3. Close all Maya windows, then open Maya again to use the new version.

Checks can also run automatically when Asset Manager opens.
Your settings and project assets are kept separate. The previous version is retained.
Test versions are installed manually and are not offered by automatic stable updates.

## Support

Report issues through this repository's Issues page. Include your Maya version, Asset Manager version, and the step that failed.

## License

MIT. See [LICENSE](LICENSE).
