# Wind-Waker-GC-Coop-Multiplayer-Guide
Instructions on how to install, connect, and play Legend of Zelda - The Wind Waker (GameCube) Coop Multiplayer with friends on the Dolphin emulator. Links to downloads will be provided as necessary.

# Installation
Join Kirbymimi's caravan (modding server):
https://discord.com/invite/ZPvZm3NFak

Go to the #mods channel and download the "New Wind Waker multiplayer (Universal)" Archive (Arc) file.
Extract the Arc.rar file.

There are instructions in the "Instructions.txt" found in the extracted Arc folder that you can follow.
You can choose to follow along with the video tutorial (outdated) provided in the instructions for visual guidance: https://youtu.be/0Bxs0bl8jSs

## Instructions
The instructions below are adopted from the former, with further clarification:
Download a US or PAL (Europe) version of The Wind Waker (GC) iso from your trusted rom site and unzip the file.
(Make sure all players have the same ROM version. Keep all files and configs consistent.)

Download the latest development version of Dolphin.
[https://dolphin-emu.org/download/]([url](https://dolphin-emu.org/download/))

Open your Dolphin dev version application (currently using: dolphin-master-2409-37-x64) and locate your iso file to open in Dolphin.
Extract the iso disc contents by:
Right clicking on The Wind Waker iso on the game list that appears in Dolphin.
Click on "Properties" and go to the "Filesystem" tab.
Right click on Disc and choose "Extract Entire Disc".

Patch the ROM "main.dol" file located in the "sys" folder located in the iso's extracted files using one of the following methods:
a) Using an external patcher tool and the included "ips" provided in the "Arc" folder:
   https://www.marcrobledo.com/RomPatcher.js/
OR
b) Alternatively, if you want to change the players' colors or don't want to use an external tool to patch the dol, you can use the "Patcher.jar" included instead. Make sure you have "Java" to run it. To run the program, open the "Patcher.jar", set the parameters you want and click "Patch!". The "Select dol" input corresponds to the original dol and "Select output" output corresponds to the path where the new dol will be created.
(Make sure the "main.dol" file in "sys" folder is replaced with the newly patched one, still named as "main.dol")

Replace your "bi2.bin" with the one in the archive depending on what ROM version (US or PAL) you have, and make sure to rename the new bin file so that it replaces the old one with the name still as "bi2.bin". Same process as with the "main.dol" file.
OR
Edit the bytes at offset 0x0004 in the "bi2.bin" file located in the "sys" folder from "0x01800000 to 0x03000000".

To use the new banner, replace the "opening.bnr" file in the files folder of your root with the one in the archive and reset the cache of the game list in the "Display" tab.

## Settings
Adjust your Dolphin settings as necessary to minimize lag and stuttering:
Click "Config" to open up Dolphin settings, and go to the "Advanced" tab.
Click "Enable Emulated CPU Clock Override".
Set the CPU's clock rate to a higher rate.
Click "Enable Emulated Memory Size Override".
Set the simulated memory size to 48mb.

# Multiplayer
Launch the "main.dol" file with Dolphin.
If the game is lagging with 4 players, try various graphics engine in the graphics settings and tweak a bit the graphics settings.

