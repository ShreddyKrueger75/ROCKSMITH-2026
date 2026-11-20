# ROCKSMITH 2026 • How I got Rocksmith 2014 running on my Apple Silicon Mac

My Steam copy of Rocksmith 2014 stopped opening on my Apple Silicon Mac running macOS Tahoe 26.6.2. I was using the CustomsForge Mac patch for custom songs. I tested a fresh copy of the app with RSBypass 1.9 attached. The patch loaded, but the game still crashed during startup under Rosetta.

What got me back to the profile screen was **RS Re-ARMed**, a community project that builds a native Apple Silicon app from your own copy of Rocksmith 2014. I installed it alongside Steam. My existing profile showed up, and I verified that all 11 Mac-format DLC archives from my Steam install copied over byte for byte. I renamed my local launcher **ROCKSMITH 2026**. The project and the installer are both called **RS Re-ARMed**. I've verified the launch and profile import. I still need to test guitar input and play through a custom song.

## How to install it

1. You’ll need an **Apple Silicon Mac (M1 or newer)**, **macOS 12 or later**, and a Steam account that owns Rocksmith 2014.
2. Grab **RS.Re-ARMed.Installer.app.zip** from the [project’s GitHub releases](https://github.com/bbelgg/rs-rearmed/releases/latest). Unzip it and open the installer. If macOS blocks the first launch, go to **System Settings → Privacy & Security** and use **Open Anyway** for that installer.
3. Choose the edition you own and click **Build & Install**. I used **Rocksmith 2014 for Mac**. If you own **Learn & Play**, choose that option and follow its [edition-specific instructions](https://github.com/bbelgg/rs-rearmed/blob/main/docs/windows/INSTALL.md).
4. When the build finishes, open **RS Re-ARMed** from your user Applications folder. The app runs offline, and progress made there is saved locally.

## How to add custom songs to the Mac edition

1. Find a song on [CustomsForge Ignition](https://ignition4.customsforge.com/) and grab its **Mac** download. The filename should end in `_m.psarc`.
2. In Finder, press **Command–Shift–G** and open `~/Library/Application Support/RS Re-ARMed/game/dlc`. Drop the file there. If you already have Mac CDLC in the Steam version’s DLC folder, the installer copies it over during setup.
3. Restart the game or select **ENUMERATE** from the main menu. Then open **Learn a Song** and look for the track.

CDLC support is built into RS Re-ARMed and enabled by default, so you can skip the separate RSBypass patch. [Mac installation and DLC documentation](https://github.com/bbelgg/rs-rearmed/blob/main/docs/mac/INSTALL.md#how-the-game-finds-dlc)

If you share this with someone, send them the project’s installer link so they can build it from their own Steam copy.

## Another option for the original Steam version

I also found [RocksmithFix](https://github.com/d1msk1y/rsfix2014-macos), a separate community patch that targets the old Steam loader used by the Intel Mac build. The author reports getting it working on an M1 running macOS Sequoia 15.8.1. I haven’t tested it on my Mac, and I didn’t find confirmation for my launch crash on Tahoe 26.6.2. The setup I verified on my Mac is the native RS Re-ARMed build.

The [author’s Reddit thread](https://www.reddit.com/r/rocksmith/comments/1y03bsg/i_brought_rocksmith_2014_on_mac_back_to_life/) has the original report.
