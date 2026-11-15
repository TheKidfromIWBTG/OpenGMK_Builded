OpenGMK_Builded

Ready-to-use Windows builds of OpenGMK, with TAS support.

OpenGMK_Builded is a Windows-focused distribution project for "OpenGMK" (https://github.com/OpenGMK/OpenGMK), a modern open-source rewrite of the proprietary GameMaker Classic engines.

Our goal is to make OpenGMK easier to download and use on Windows by automatically building and publishing its essential emulator executables.

✨ Features

- Automated Windows builds: binaries are compiled and published automatically through GitHub Actions.
- 64-bit support: includes "gm8emulator.exe".
- WoW64 support: includes "gm8emulator-wow64.exe" for compatibility with 32-bit native DLLs on 64-bit Windows.
- TAS functionality: retains the TAS recording and playback framework provided by OpenGMK.
- Upstream tracking: builds are generated from commits of the original OpenGMK repository.

📥 Download

"Download the latest OpenGMK_Builded release" (https://github.com/TheKidfromIWBTG/OpenGMK_Builded/releases/latest)

Each release provides a ZIP archive containing:

File| Description
"gm8emulator.exe"| Main 64-bit emulator
"gm8emulator-wow64.exe"| 32-bit WoW64 helper

Installation

1. Download the latest ZIP archive from Releases.
2. Extract its contents into a folder.
3. Keep both executables together in the same directory.
4. Run "gm8emulator.exe".

The WoW64 helper is used when games require 32-bit native DLLs, such as certain audio extensions.

🎮 Using OpenGMK for TAS

OpenGMK includes a framework for recording and replaying Tool-Assisted Speedruns (TAS).

Playing a game

Run the emulator with the path to a compatible GameMaker Classic game:

gm8emulator path/to/game.exe

Starting or continuing a TAS project

Use "-n" followed by a project name:

gm8emulator path/to/game.exe -n project-name

A project folder will be created to store recording data and savestates.

Replaying and exporting recordings

OpenGMK uses ".gmtas" files to store input data for sharing TAS recordings.

To recreate a savestate from a recording:

gm8emulator path/to/game.exe -l -f path/to/save.gmtas -o path/to/save.bin

For more detailed information about TAS functionality, consult the "original OpenGMK repository" (https://github.com/OpenGMK/OpenGMK).

⚙️ Automated Builds

OpenGMK_Builded uses GitHub Actions to:

1. Check the latest commit in the original OpenGMK repository.
2. Download the corresponding source code.
3. Compile the 64-bit emulator.
4. Compile the WoW64 helper.
5. Package the executables into a ZIP archive.
6. Publish a GitHub Release.

The workflow periodically checks for upstream updates and can also be started manually.

Each release identifies the original OpenGMK commit used to produce the binaries.

⚠️ Important Information

OpenGMK is a work in progress. Some games or engine features may not yet be fully supported.

- GameMaker: Studio games are not supported; OpenGMK targets GameMaker Classic.
- OpenGMK currently requires OpenGL 3.3 with GLSL 3.30 support.
- Savestates may become incompatible between different OpenGMK versions.
- The WoW64 helper is intended for 64-bit Windows systems that need 32-bit native DLL compatibility.

This project distributes automatically compiled binaries. It does not guarantee that every GameMaker Classic game will work correctly.

🔗 Original Project

OpenGMK_Builded is based on the original "OpenGMK" (https://github.com/OpenGMK/OpenGMK) project.

All original engine functionality and development belong to the upstream project and its contributors.

Please visit the original repository for source code, documentation, development information, and contributions.

🤝 Credits

Thanks to the original OpenGMK developers and contributors for creating and maintaining this project.

Additional original credits can be found in the "OpenGMK repository" (https://github.com/OpenGMK/OpenGMK).

📜 License

OpenGMK is distributed under the GNU General Public License v2.0 (GPL-2.0-only).

OpenGMK_Builded follows the licensing terms of the original project.

OpenGMK_Builded is an independent distribution project and is not affiliated with, endorsed by, or officially connected to GameMaker or YoYo Games.
