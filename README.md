# Wind-Waker-GC-Coop-Multiplayer-Guide
Instructions on how to install, connect, and play Legend of Zelda - The Wind Waker (GameCube) Coop Multiplayer with friends on the Dolphin emulator. 

Links to downloads will be provided as necessary.

## Installation
Join the Kirbymimi's modding server on [Discord](https://discord.com/invite/ZPvZm3NFak).

Go to the #mods channel and download the "New Wind Waker multiplayer (Universal)" Archive (Arc) file.

Unzip the Arc.rar and read instructions. The instructions are in the "Instructions.txt" found in the extracted Arc folder. You can choose to follow along with the [video tutorial (outdated)](https://youtu.be/0Bxs0bl8jSs) provided in the txt file for visual guidance.

## Instructions
Download a US or PAL (Europe) version of The Wind Waker (GC) iso from your trusted rom site and unzip the file.

**Make sure all players have the same ROM version. Keep all files and configs consistent.**

Download the latest **development version** of [Dolphin](https://dolphin-emu.org/download/). (Currently using: Dolphin 2409-37) 

Open your Dolphin application and locate your iso file to open up in Dolphin.

Extract the iso disc contents:
- Right click on The Wind Waker ROM on the game list that appears in Dolphin's main window.
- Click on "Properties" and go to the "Filesystem" tab.
- Right click on Disc and choose "Extract Entire Disc".

Patch the ROM "main.dol" file located in the "sys" folder located in the iso's extracted files using one of the following methods:
- Using an external patcher tool and the included "ips" provided in the "Arc" folder:
   https://www.marcrobledo.com/RomPatcher.js/

OR

- Alternatively, if you want to change the players' colors or don't want to use an external tool to patch the dol, you can use the "Patcher.jar" included instead. Make sure you have "Java" to run it. To run the program, open the "Patcher.jar", set the parameters you want and click "Patch!". The "Select dol" input corresponds to the original dol and "Select output" output corresponds to the path where the new dol will be created.

**Make sure the "main.dol" file in "sys" folder is replaced with the newly patched one, still named as "main.dol".**

Replace your "bi2.bin" with the one in the archive depending on what ROM version (US or PAL) you have, and make sure to rename the new bin file so that it replaces the old one with the name still as "bi2.bin". Same idea as with the "main.dol" file.

OR

Edit the bytes at offset 0x0004 in the "bi2.bin" file located in the "sys" folder from "0x01800000 to 0x03000000".

To use the new banner, replace the "opening.bnr" file in the files folder of your root with the one in the archive and reset the cache of the game list.

## Settings
Adjust your Dolphin settings as necessary to minimize lag and stuttering:

Click "Config" to open up Dolphin settings

In the "General" tab:
- Check "Enable Dual Core (speedhack)".

Go to the "GameCube" tab.
- Under "Device Settings", change "Slot A" to "Memory Card".

Go to the "Advanced" tab.
- Click "Enable Emulated CPU Clock Override".
- Set the CPU's clock rate to a higher rate.
- Click "Enable Emulated Memory Size Override".
- Set the simulated memory size to 48mb.

If the game is lagging with 4 players, try various graphics engine in the graphics settings and tweak a bit the graphics settings.

### 16:9 Aspect Ratio
Click "Config" to open up Dolphin settings
- In the "General" tab, check "Enable Cheats".
  
Right click the game in your game list and choose "Properties".
- Go to "Gecko Codes" tab.
- Click "Add New Code..." and add the [16:9 Aspect Ratio Fix](https://wiki.dolphin-emu.org/index.php?title=The_Legend_of_Zelda:_The_Wind_Waker) code depending on your ROM version.
- Make sure the code is enabled with a checkmark on the left.

### Graphics Mod
- [Hypatia’s Hi-Res Wind Waker Texture Pack Version 2.0
](https://onthegreatsea.tumblr.com/DOWNLOADS)

## Controller
Click "Config" to open up Dolphin settings
- Go to "Interface" tab, and change "Mouse Cursor Visibility" to "Never".

In Dolphin's main window, click "Controllers".
- Click "Configure" under "GameCube Controllers".
- Select your device (Gamepad) from the "Device" drop down menu. Refresh if you don't see it.
- The "C Stick" controls the camera. So remap and calibrate as necessary. Switch the "Right X+" and "Right X-" for inverted camera controls.

# Multiplayer
Launch the "main.dol" file with Dolphin.

## Host
Set up for hosting:
- Click "Tools" and "Start Netplay..."
- Edit your "Nickname".
- Click "Host".
- Check "Forward port (UPnP)".
- Select The Wind Waker ROM.
- Share your [IP address](https://whatismyipaddress.com/) (ie. IPv4) to your friends to connect to.
- Click "Start" when all players have joined.

If you already have your network configs set up, the shortcut is:
- Right click The Wind Waker ROM in Dolphin's game list display.
- "Host with NetPlay"

## Connect
To connect to the host as a client:
- Click "Tools" and "Start Netplay..."
- Edit your "Nickname".
- Input the host's IP address.
- Click "Connect".

## Sun Glare Lag
All players must do this. Launch the game together through the Netplay lobby.
- Go back to the main Dolphin window, and open the "Graphics" settings.
- Under the "Hacks" tab, make sure "Skip EFB Access from CPU" is checked.

This setting rests to unchecked every time you launch the game, so you have to do this after it's already running.
