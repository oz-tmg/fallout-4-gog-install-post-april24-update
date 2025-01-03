# fallout-4-gog-install-post-april24-update
Used to help organize my trials and tribulations of trying to get Fallout 4 working on my M2 Apple Silicon Mac Mini post Bethesda update April 11th 2024.

## Sources
I mostly worked off the following guides:
- [Macgaming reddit post](https://www.reddit.com/r/macgaming/comments/1718p7t/comment/kzr2lrk/)
- [Fallout 4 Next-Gen on Mac Tutorial by Andrew Tsai](https://www.youtube.com/watch?v=dQYop_gICmc)
- [The Midnight Ride mod guide for FO4](https://themidnightride.moddinglinked.com/setup.html)

## Requirements
1. Fallout 4 GOTY 1.10.163 GOG Version (includes all DLCs)
2. Crossover
3. At least 52GB of free drive space, game included (45GB if you delete all the downloads).

## Setup
1. Purchase Fallout 4 GOTY version on GOG.  Steam doesn't work well with mods since the update.
2. Download the offline files for Fallout 4.  This will take a while. 
3. Get Crossover and install it.
4. Create a new bottle in Crossover (Cmd + N) and name it "Fallout 4 - GOG Offline."
5. Put the install files into a new folder ("GOG Games") in the c_drive found in the bottle.
   - Path looks like this: `/Users/<username>/Library/Application Support/CrossOver/Bottles/Fallout 4 - GOG Offline/drive_c/GOG Games`
6. Install the game into the Fallout 4 bottle (search it on crossover) with bottle version win10 64bit.
  - 
7. Enable DXVK, Esync, add the x-audio libraries, mouse fix in Crossover
8. Edit Wine Configuration by going into Libraries and add the following to the overrides:
   - xaudio2_6
   - xaudio2_7
   - x3audio1_6
   - x3audio1_7
10. Get BethINI
11. Choose the High BethINI preset as the guide suggests, but DISABLE GOD RAYS. They cause a visual glitch.
12. CHANGE ambient occlusion from “HBAO+” to “SSAO” as it causes the game to be black screen.
13. Edit Launch Parameters
   7.1.   Open Crossover on your Mac Mini
   7.2.   Locate the Bottle where Mod Organizer 2 is installed.
   7.3.   Open the "Run Command" or the "Advanced Options" for that Bottle (depending on your Crossover version).
   7.4.   Run Mod Organizer from Crossover.
   7.5.   In Mod Organizer, Click on the Gears icon (right next to the executable selection dropdown at the top) to open Executables settings.  This is where you can edit how Mod Organizer launches applications like Skyrim, Fallout, etc.
   7.6.   Under Executables, find F4SE, look for the "Arguments" field ("Command Line Parameters"), and enter launch parameter `-forcesteamloader`.  This enure the Mod Organizer will pass the parameter when it launches the game.  

### Game Settings: BethINI
Change and optimize presets and more specific options:
1. Download Bethini Pie.
2. Extract the archive anywhere outside of the default Windows folders, such as C:\Modding Tools.
3. In MO2, click on the drop-down in the right pane next to the Run button.
4. Click <Edit...>, then click the + symbol in the top left and Add from file.
5. In the resulting explorer window, navigate to where you installed Bethini Pie and select Bethini.exe.
6. Press Apply in the lower right, then OK.
7. Select Bethini from the drop-down and run it.
8. Click Fallout 4 then press Select Game.
9. If you get a Setup prompt press OK. You don't need to redirect the INI path to MO2's profile folder because MO2's VFS already handles the redirection.
10. Apply the following settings:
    - Select a Bethini preset depending on your hardware.
    - The Bethini High preset is recommended for most systems, use Ultra if you have spare GPU performance and want better visual quality.
    - You can check this complete comparison if you are unsure.
    - Apply Recommended Tweaks.
    - Set Display Mode to Borderless Windowed.
    - Select the resolution you want to display the game in.
    - Make sure Text Language is set to English both in Bethini Pie and on Steam (other languages are not supported by the guide).
    - DISABLE GOD RAYS. They cause a visual glitch.
    - CHANGE ambient occlusion from “HBAO+” to “SSAO” as it causes the game to be black screen. 
    - Edit the other settings to your liking.
11. Click File then Save in the top left, then confirm the prompts and close Bethini.

## Mod Organizer 

### Installing Mod Organizer 2 in some simple steps:
- Download Mod Organizer 2 from [here](https://www.nexusmods.com/site/mods/874).
- Once the download has finished, run the installer.
- Accept the license, click Next.
- When asked about the install location, change MO2 to The Midnight Ride and click Next.
- On the install components page, use defaults.
- When asked about the Start Menu folder, change the name to The Midnight Ride and click Next.
- Change the name to The Midnight Ride
- Don't create a Desktop shortcut - we will create our own later.
- On the final page, click Install.
- Once the installation is complete, ensure that Launch Mod Organizer is ticked and click Finish.

### Setup
1. On the install components page, use defaults.
2. On the instance creation page, select Create a portable instance, click Next.
3. Select Portable Instance option
4. Select Fallout 4 and click Next.
5. Select the store where you bought the game, click Next.
6. When asked about profile settings, enable all options and click Next.
7. Keep the default location file path.
8. Click Connect to Nexus.

If you have MO2 installed on an SSD or a HDD with little space, you can check the Show advanced options box and change the Downloads file path to a different drive with more space. This will not affect the game's performance, the downloaded files can be deleted after the mods have been installed.

9. On the last page, select Finish.
10. If you see a pop-up called Show tutorial?, select No.
11. If you see a pop-up called Register?, select Yes.
12. If you see a pop-up called INI file is read-only, select Remember my choice from the drop-down at the bottom then click Clear the read-only flag.

### Configuring Settings
1. Click the X in the bottom right of MO2 to close the log window.
2. Click the MO2 settings button at the top of MO2 to open the settings.
3. If you wish, you can select a different theme.
4. In the Nexus tab, select Connect to Nexus.
5. Connect to Nexus

This option will not show up if you have already connected your Nexus account on a different MO2 instance.

MO2 will open your browser and prompt you to authorize the connection.  Once you authorize it, you can close your browser and of the MO2 settings.  Allow MO2 to restart.


### Fallout 4 Script Extender (F4SE)
Extends the scripting capabilities of the game.
Installation instructions

    Main Files - Fallout 4 Script Extender (F4SE) 0.6.23
        Open the downloaded archive and move everything to the game's Root folder.

    If you do not know what the Root folder is, read the Key Terminology.

    The direct link to an older version is intentional to grant compatibility with the downgraded EXE.

    Downloading through the link button above is especially important when the guide specifies the exact version, like for this mod and more later.
        After proper install, your Root folder should look like this:
        Root folder with a correct F4SE install

### xSE PluginPreloader F4
Allows preloading F4SE plugins before the game initializes.
Installation instructions

    Main Files - xSE PluginPreloader F4 0.2.5.1
        Open the downloaded archive and move everything to the game's Root folder.

### Simple Fallout 4 Downgrader
A simple one-click downgrader that doesn't require any login credentials.
Installation instructions

    Main Files - Simple Fallout 4 Downgrader - for v1.10.984
        Open the downloaded archive and extract everything to the game's Root folder.
        Double-click on fo4downgrader.exe to run it.
        A command prompt window will open and it should say:
        Patching successful
        Close the command prompt and backups with _downgradeBackup appended to their name should appear in the game's Root folder.


Making MO2 Detect F4SE

    Once F4SE is installed as instructed above, restart MO2 and you should see a new option in the top right drop-down.
    ![image](https://github.com/user-attachments/assets/e5a1ae6c-19c6-4858-bac7-b1c3d35c85c2)
