PrusaSlicer:

; M190 S0
; M109 S0 ; uncomment to remove set&wait temp gcode added automatically after this start gcode
print_start HOTEND=[first_layer_temperature[initial_tool]] BED=[first_layer_bed_temperature]

cura:

PRINT_START BED={material_bed_temperature_layer_0} HOTEND={material_print_temperature_layer_0}

SuperSlicer:

; M190 S0
; M109 S0 ; uncomment to remove set&wait temp gcode added automatically after this start gcode
print_start HOTEND={first_layer_temperature[initial_extruder] + extruder_temperature_offset[initial_extruder]} BED=[first_layer_bed_temperature] CHAMBER=[chamber_temperature]
