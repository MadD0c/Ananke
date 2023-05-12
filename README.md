# klipper-macros



###############################
### Filament Switch Sensor ####
### https://www.klipper3d.org/Config_Reference.html#filament_switch_sensor ###
###############################
#[filament_switch_sensor filament_sensor]
#switch_pin: ^PB6
#pause_on_runout: False ; pause handled by macro
#runout_gcode:
#  FILAMENT_RUNOUT ; trigger filament runout
#insert_gcode:
#  LOAD_FILAMENT ; trigger filament load

###############################
### Filament Motion Sensor ####
### https://www.klipper3d.org/Config_Reference.html#filament_motion_sensor ###
###############################
#[filament_motion_sensor smart_filament_sensor]
#switch_pin: ^PB6
#detection_length: 7.0
#extruder: extruder
#pause_on_runout: False ; pause handled by macro
#runout_gcode:
#  FILAMENT_RUNOUT ; trigger filament runout
#insert_gcode:
#  LOAD_FILAMENT ; trigger filament load

Here is how the above example would work in this new format:

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