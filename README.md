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