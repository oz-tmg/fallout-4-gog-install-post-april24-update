# fallout-4-gog-install-post-april24-update
Used to help organize my trials and tribulations of trying to get Fallout 4 working on my M2 Apple Silicon Mac Mini post Bethesda update April 11th 2024.

## Sources
I mostly worked off the following guides:
- [Macgaming reddit post](https://www.reddit.com/r/macgaming/comments/1718p7t/comment/kzr2lrk/)
- [Fallout 4 Next-Gen on Mac Tutorial by Andrew Tsai](https://www.youtube.com/watch?v=dQYop_gICmc)
- [The Midnight Ride mod guide for FO4](https://themidnightride.moddinglinked.com/setup.html)

## Requirements
1. Fallout 4 GOTY 1.10.163 GOG Version
2. Crossover

## Setup
1. Install the game into the Fallout 4 bottle (search it on crossover) with bottle version win10 64bit.
2. Enable DXVK, Esync, add the x-audio libraries, mouse fix in Crossover
3. Edit Wine Configuration by going into Libraries and add the following to the overrides:
   - xaudio2_6
   - xaudio2_7
   - x3audio1_6
   - x3audio1_7
4.  
