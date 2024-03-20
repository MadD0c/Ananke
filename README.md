<h1 align="center">
!!!!!  I have been doing a lot of changes to this over the last few weeks so unfortunatly the Wiki is a bit out of date.
Please be patient while I get it updated
Thanks !!!!!!!
</h1>

<h1 align="center">
Ananke
</h1>

>Ananke is the powerful deity that rules compulsion, constraint, restraint, or coercion, and presides over all forms of slavery and bonds, starting with the basic necessities of life. Consequently, when someone is cast into prison, or fastened by chains, her name is evoked. For she is behind all bonds, and has a share even in the ties of kinship, friendship and love. She is called Necessity, since once the attachment is established there cannot but follow what necessarily is derived from it, her might allowing no resistance.[^1]

These are the klipper macros for my pantheon of printers. 

I initially started working on them with my first printer - Theseus (Kliperized Ender3 V2). Since construction of Deadalus (Voron Trident 300mm) I have made numerous extensions to make it more versatile and adaptable. 

Settings and print variables are all managed via macro variables. This allows them to be adjusted as needed at the time of print or on the fly.

The foundation for this collection (as well as the inspiration) comes from [Rootiest's Zippy-Klipper-Config](https://github.com/rootiest/zippy-klipper_config). I have supplemented and addapted his work with: 
- ~~Compatibility with the complete version of [KAMP](https://github.com/kyleisah/Klipper-Adaptive-Meshing-Purging)~~ (Removed in favour of Klipper's built in adaptive meshing
- A notification system which works directly with moonraker's notify
- ~~LED templating by [digitalninja-ro](https://github.com/digitalninja-ro/klipper-neopixel)~~ (Changed to [Klipper LED Effects](https://github.com/julianschill/klipper-led_effect) as more adaptable)
- Nozzle cleaning macros from [edwardyeeks Decontaminator Purge Bucket Nozzle Scrubber Mod](https://github.com/VoronDesign/VoronUsers/tree/master/orphaned_mods/printer_mods/edwardyeeks/Decontaminator_Purge_Bucket_%26_Nozzle_Scrubber)
- Interuptable Heat Soak system by ([garethky](https://github.com/garethky/klipper-voron2.4-config/blob/mainline/printer_data/config/heatsoak.readme.md))
- Partial Support for [NozzleChanger](https://github.com/garethky/change-nozzle-klipper-extra) (Still working on adjusting Pressure Advance based on Nozzle and checking in Start Macro)
- Innitial Support for [Build Sheet Manager & “Adjust Live Z”](https://klipper.discourse.group/t/build-sheet-manager-adjust-live-z/4013) (Still needs clean up in Start Macro)

## Requirements
Please see the [Wiki](https://github.com/MadD0c/Ananke/wiki/Requirements) for details.
## Installation
Please see the [Wiki](https://github.com/MadD0c/Ananke/wiki/Installation) for details.
## Configuration
Please see the [Wiki](https://github.com/MadD0c/Ananke/wiki/Configuration) for details.
## Updating
Please see the [Wiki](https://github.com/MadD0c/Ananke/wiki/Updating) for details.

## To-Do
I have a few upcoming plans for improving this collection. Unfortunately I have not got a timeline for now as it all depends on me implementing them on Daedalus
- ~[X] Add Support for [NozzleChanger](https://github.com/garethky/change-nozzle-klipper-extra)~
- ~[X] Add Support for [Build Sheet Manager & “Adjust Live Z”](https://klipper.discourse.group/t/build-sheet-manager-adjust-live-z/4013)~
- [ ] Add Support for [Spoolman](https://github.com/Donkie/Spoolman)
- [ ] Add Support for [Filament Handling Macros](https://github.com/garethky/klipper-voron2.4-config/blob/mainline/printer_data/config/filaments.readme.md)
- [ ] Add Support for [ERCF](https://github.com/EtteGit/EnragedRabbitProject)
- [ ] Ultimaker Cura Support

  [^1]:https://www.maicar.com/GML/Ananke.html
