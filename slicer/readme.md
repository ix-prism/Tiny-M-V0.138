切片配置文件建议套用Voron0.1或2.4的预设，并将平台大小改为150x150，高度150。

并更改打印机设置中的：

起始Gcode:

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

结束Gcode:

print_end
