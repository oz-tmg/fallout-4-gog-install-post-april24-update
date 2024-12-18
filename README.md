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
1. Install the game into the Fallout 4 bottle (search it on crossover) with bottle version win10 64bit.
2. Enable DXVK, Esync, add the x-audio libraries, mouse fix in Crossover
3. Edit Wine Configuration by going into Libraries and add the following to the overrides:
   - xaudio2_6
   - xaudio2_7
   - x3audio1_6
   - x3audio1_7
4. Get BethINI
5. Choose the High BethINI preset as the guide suggests, but DISABLE GOD RAYS. They cause a visual glitch.
6. CHANGE ambient occlusion from “HBAO+” to “SSAO” as it causes the game to be black screen.
7. Edit Launch Parameters
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


