# Asset Manager

A Maya tool for browsing, publishing, and reusing versioned assets.

## Download

**Asset Manager v0.1.9** for Mac and Windows.

Click the ZIP download for your computer:

| Your computer | Download | Maya versions |
| --- | --- | --- |
| Mac | [Download for Mac (.zip)](https://github.com/brianlaiii/AssetManager-releases/releases/download/v0.1.9/asset-manager-0.1.9-macos.zip) | 2024, 2026, 2027 |
| Windows | [Download for Windows (.zip)](https://github.com/brianlaiii/AssetManager-releases/releases/download/v0.1.9/asset-manager-0.1.9-windows.zip) | 2024, 2025, 2026, 2027 |

The ZIP is ready to use in Maya. You do not need GitHub login, Git, a separate Python installation, or a build step.
Both links download the ready-to-install ZIP directly.

This version repairs missing or damaged Arnold JPEG previews from existing EXRs when you open a clip. It updates the JPEG count in the Media List as previews become available.
Auto repair and cache reuse were checked in Mac Maya 2024. Windows Maya, OneDrive rendering, and Windows playback speed remain unverified.

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

## Arnold media previews

Arnold media keeps raw EXR images separately from JPEG player previews.
Choose **Media > Arnold Render** and select your frames. **Frames to Render** shows the selected range and count. JPEG previews use the Python and image tools supplied with Maya; no separate package installation is needed.

Open an Arnold clip with **View > Image Source > Auto** to repair previews in the background. Auto prioritizes the current frame and uses the saved render view. Writable temporary jobs save repaired previews beside the EXRs. Published and locked clips use a local disk cache. Reopening reuses the JPEGs already repaired. The first pass can take time with Maya's built-in converter.

Choose **JPEG Preview** to review JPEGs or **Original EXR** to read the source images directly. For a temporary job, **Media > Open Recent Tmp Media > Retry JPEG Previews** can also rebuild previews from existing EXRs.

## Support

Open **Settings > Problem Reports > Report a Problem**, or **Help > Report a Problem**.

1. Describe what happened and what you expected.
2. Click **Preview Report** and review the text before sharing it.
3. Click **Export ZIP** and choose where to save it.
4. Send the ZIP privately to the person helping you. **Show in Folder** opens its location.

The report includes app and system versions, recent Asset Manager activity, and observed errors.
Common credentials, email addresses, and absolute paths are filtered. Review your description and report for other private information.
Scene files, textures, settings files, and screenshots are not attached.
Activity is retained locally with a size limit, starting when this version opens. Earlier actions may be unavailable.
Export does not require a GitHub account and does not send or upload anything automatically.

You can also report issues through this repository's Issues page. Avoid posting diagnostic reports publicly when they contain private information.

## License

MIT. See [LICENSE](LICENSE).
