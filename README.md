# Icarus

These are the klipper macros for my panthion of printers. Initially started working on them with my first printer - Theseus (Kliperized Ender3 V2). Since construction of Deadalus - Voron Trident 300mm I have made numerous extensions to make it more versitile.

Settings and print variables are all managed via macro variables. This allows them to be adjusted as needed at the time of print or on the fly.

The foundation for this collection (as well as the inspiration) comes from Rootiest's Zippy-Klipper-Config (https://github.com/rootiest/zippy-klipper_config). I have supplimented his work with: 
the complete version of KAMP
an notification system which works directly with moonraker's notify
LED templating by digitalninja-ro (https://github.com/digitalninja-ro/klipper-neopixel)
Nozzle cleaning macros from edwardyeeks Decontaminator Purge Bucket Nozzle Scrubber Mod(https://github.com/VoronDesign/VoronUsers/tree/master/orphaned_mods/printer_mods/edwardyeeks/Decontaminator_Purge_Bucket_%26_Nozzle_Scrubber)

#    Requrements

#    Installation

#    Configuration

#    Slicer Steup

    SET_GCODE_VARIABLE MACRO=_printcfg VARIABLE=extruder_temp VALUE={first_layer_temperature[initial_extruder] + extruder_temperature_offset[initial_extruder]}
    SET_GCODE_VARIABLE MACRO=_printcfg VARIABLE=bed_temp VALUE={first_layer_bed_temperature[initial_extruder]}
    SET_GCODE_VARIABLE MACRO=_printcfg VARIABLE=layer_count VALUE={total_layer_count}
    SET_GCODE_VARIABLE MACRO=_printcfg VARIABLE=tool_count VALUE={total_toolchanges}
    SET_GCODE_VARIABLE MACRO=_printcfg VARIABLE=nozzle_size VALUE=0.4 ; Manually set 
    START_PRINT

Before layer change
    SET_GCODE_VARIABLE MACRO=_printcfg VARIABLE=layer_num VALUE={layer_num}
    SET_GCODE_VARIABLE MACRO=_printcfg VARIABLE=layer_z VALUE={layer_z}
    LAYER_CHANGE_BEFORE

After layer change
    SET_GCODE_VARIABLE MACRO=_printcfg VARIABLE=layer_num VALUE={layer_num}
    LAYER_CHANGE_AFTER

End Print
    END_PRINT

With each Filament preset
    SET_GCODE_VARIABLE MACRO=_printcfg VARIABLE=material_type VALUE={filament_settings_id[0]}
    SET_GCODE_VARIABLE MACRO=_printcfg VARIABLE=material_color VALUE={filament_colour}
    SET_GCODE_VARIABLE MACRO=_printcfg VARIABLE=nevermore VALUE=False
    SET_GCODE_VARIABLE MACRO=_printcfg VARIABLE=use_scrubber VALUE=False
    SET_GCODE_VARIABLE MACRO=_printcfg VARIABLE=chamber_temp VALUE={chamber_temperature} ;exclude in Prusaslicer or set manually
