# Yuzu EA Update from pineappleEA
This is a simple modified version of the original yuzu.sh file to allow update from pineappleEA instead of the original yuzuEA. Use this at your own risk. I do not know if EmuDeck update will break this in the future. All I did was add the pinappleEA API to the host and remove all of the token and BEARER header. Everything else is still the same as the original. I added a check if there's no yuzu-ea.AppImage install, and 'useEA=True' is set, then it will download the latest pineappleEA. 

## Files
[yuzu.sh](https://github.com/mrmikey05/yuzuEAUpdate/blob/main/yuzu.sh) is a drop-in replacement of your original and will continue to update your pineappleEA to the latest when there's one available.

## How to use this
**Backup your original yuzu.sh** in /Emulation/tools/launchers. I recommend making a copy of it and renaming it to yuzu-origin.sh or something in case there's issue. If you install EmuDeck on your internal drive, then it will be in the HOME. If it SD Card, then it will be in the Primary.

Either replace your yuzu.sh with the one here or replace the content inside your yuzu.sh with the content inside this yuzu.sh. 
To replace it, download the yuzu.sh [here](https://github.com/mrmikey05/yuzuEAUpdate/blob/main/yuzu.sh). Place it in your /Emulation/tools/launchers folder. Right click and select property. Go to the Permissions tab and check **Is Executable**. Make sure it is named yuzu.sh. If you don't have the yuzu-ea.AppImage install, run the script and it will automatically install it for you. If you already have one and not sure if it outdated, you should just run your yuzu-ea.AppImage as normal and the script will see if there's a update for it or not.

## Configuration
I added a configuration to check if there's a Early Access file (yuzu-ea.AppImage) and if not, it will download automatically. If you do not wish to use Early Access and stick with Mainline, set the `useEA=True` to `useEA=False`. It is set to **True** by default. 

## Revert back to default
If you want to revert back to default, you can get the default yuzu.sh from [EmuDeck Github](https://github.com/dragoonDorise/EmuDeck/blob/main/tools/launchers/yuzu.sh). Either download and replace it or copy the content inside and paste in over your yuzu.sh file.
