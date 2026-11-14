# WheatlyCube

A controller-friendly game library for Windows, Linux / Steam Deck and Android that plays your
games from a [RomM](https://github.com/rommapp/romm) server: browse your consoles, see box art,
descriptions and trailers, and launch each game in the right emulator.

**This repository holds downloads only.** Get the latest version from
[Releases](../../releases/latest).

## Install

**Windows**

1. Download `WheatlyCube-<version>-setup.exe` from the [latest release](../../releases/latest).
2. Run it. Windows may say **"Windows protected your PC"** because the installer isn't
   code-signed yet: click **More info**, then **Run anyway**.
3. Pick the theme and sound packs you want (all of them is fine), and finish.

**Steam Deck and other Linux PCs**

1. In Desktop Mode, download `WheatlyCube-<version>-x86_64.AppImage` into `~/Applications`.
2. Make it executable (right-click > Properties > Permissions > **Is executable**) and run it
   once to sign in to RomM.
3. Steam > Games > **Add a Non-Steam Game**, pick the AppImage, and add `--fullscreen` to its
   Launch Options. Play it from Game Mode like any game.

**Android (phones, tablets, the AYN Thor)**

1. Download `WheatlyCube-<version>-android-arm64.apk` on the device and open it. Allow your
   browser or file manager to install apps when Android asks.
2. After signing in, open **Settings > Playing > Emulator setup**: it installs the emulators from
   your RomM server (when they are kept there), copies the BIOS files and lists the one-time
   steps inside each emulator.

## First start

1. WheatlyCube opens a short setup. Choose **Connect to RomM**.
2. Enter the RomM address you were given (it starts with `https://`). Then sign in one of two
   ways, both made on the RomM website (open the same address in a browser and log in):
   - **Pairing code** (easiest): in RomM, open your user menu and make a device pairing code,
     then type the 8 digits into WheatlyCube.
   - **API key:** in RomM's user settings, create an API key and paste it in.
3. Pick where WheatlyCube keeps its files (games you download, emulators, saves). A folder on
   a big drive is best.
4. Open a console, pick a game and press **A** (or Enter). The first time a console needs an
   emulator, WheatlyCube offers to install it from the emulator's official site.

Controls: arrows or the left stick to move, **A** to choose, **B** to go back, **Start** for the
menu, **X** for details, **Y** for a random game. Hold **A** for launch options (choose how to play this time).

## Playing straight from the server

Pick **Play over the network** to stream a game from the RomM server instead of downloading it
first: only the parts the emulator reads come down. On Android it needs no setup. On Linux,
open **Settings > Playing > Streaming through RomM** and press **Download rclone**, then
**Test streaming**. On Windows it needs WinFsp (free) once: open
**Settings > Playing > Streaming through RomM**, press **Install WinFsp** (Windows asks for
permission), then **Download rclone** and **Test streaming**. Nothing else to set up: it uses the
same RomM address and sign-in.

## Updates

WheatlyCube checks this page for new versions and offers them in **Settings > System** (Windows)
and updates the AppImage by itself (Linux). On Android, install the new APK over the old one.

New games and new art on the RomM server show up by themselves: WheatlyCube checks RomM when it
starts and every 15 minutes. To check straight away, use **Settings > Library > Update library**.

## Something wrong?

Turn on **Settings > System > Debug logging**, make the problem happen again, turn it off, then
press **Make bug report** and send the file it makes. Passwords, keys and server addresses are
left out of the report.

## Credits

WheatlyCube started from [Freegosy](https://github.com/abduznik/Freegosy) by abduznik (MIT
licence). Emulators, BIOS files and games are not included and are your own responsibility.
