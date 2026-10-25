# Red Alert 2 Native ARM64 for Android

Red Alert 2 and Yuri's Revenge in one Android APK, with the original campaign maps, movies and game data. This is an unofficial native ARM64 development port using statically recompiled game logic, SDL2 and a native Windows API compatibility layer.

**Version:** 0.1.4-native-development (version code 5)

**Package:** `com.ascendes.ra2native`

**Download size:** approximately 1.85 GB (1,849,968,813 bytes)

[**Download the APK**](https://github.com/AscendesShady/RA2_APK/raw/refs/heads/main/Red-Alert-2-Native-ARM64.apk) | [**Input and controls guide**](INPUTS.md)

## Requirements

- An ARM64 Android device running Android 8.0 or newer.
- At least 6 GB of free storage before downloading and installing; updates may need more temporary space.
- Intended devices include Samsung Galaxy Tab S9 Ultra and Galaxy S24 Ultra. Physical-device performance and S Pen behavior still need verification.

## Install

1. Download `Red-Alert-2-Native-ARM64.apk` using the link above. Download the actual APK, rather than saving the GitHub webpage.
2. Open it using your browser's download list or an Android file manager.
3. If Android requests permission, allow that browser or file manager to install apps, then continue with **Install**.
4. Open **Red Alert 2 Native** and choose **Play Red Alert 2** or **Play Yuri's Revenge**.
5. Let the first launch prepare the bundled game files. Preparation is local and can resume after interruption.
6. Choose **Single Player > New Campaign** or **Skirmish** in the original game menu. No separate game-data download is required after installing this APK.

### Update without losing saves

Install this APK over the existing app signed with the same key. **Do not uninstall the app or clear its storage when updating**: saves are held in the app's private storage.

## Save, load and exit

- Open the mission menu with **Menu / Esc** or a quick three-finger tap, then choose **Save Game**.
- The name is filled automatically with the current mission followed by local date and time, for example `Operation: Lone Guardian - 2026-10-16 15:20:02`. No keyboard or typing is required.
- Tap **Save**, acknowledge **Mission Saved** with **OK**, then choose **Resume Mission**.
- Use **Load Game** in the original menu to select a saved game for the corresponding title.
- **Exit Game** returns to the Android chooser for Red Alert 2 and Yuri's Revenge.

See [INPUTS.md](INPUTS.md) for touch, S Pen, OTG/Bluetooth mouse and toolbar instructions.

## File verification

The APK SHA-256 is:

```text
e0e7170180888d26c09836ac33f01d61a9498b846e7b39d43399400ed4b16b30
```

This APK is tracked with **Git LFS** because of its size. For a developer checkout:

```sh
git lfs install
git clone https://github.com/AscendesShady/RA2_APK.git
cd RA2_APK
git lfs pull
```

If a downloaded `.apk` is only a few hundred bytes or starts with `version https://git-lfs.github.com/spec/v1`, it is an LFS pointer, not the installer. Use the direct download link above or `git lfs pull`.

## Verification limits

The recorded emulator checks include campaign starts and save/reload in both games. Version 0.1.4 also passed save-name formatting, complete-name persistence, APK signature/alignment and existing-save preservation checks. Full campaign playthroughs, long sessions, audible sound and physical Samsung/OTG/S Pen behavior have not been established by those checks. This is a locally signed, debuggable development build; multiplayer is not enabled.

## Credits

Command & Conquer: Red Alert 2 and Yuri's Revenge are Westwood / Electronic Arts titles. This unofficial package includes the game copy supplied for this project. Runtime components include redalert2-recomp, pcrecomp, SDL2, SDL2_ttf, FreeType and FFmpeg. Open **Credits and licences** in the Android launcher for bundled notices and licence texts.
