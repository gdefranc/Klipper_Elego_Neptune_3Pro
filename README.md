# Klipper_Elego_Neptune_3Pro
This is my settings for Klipper.

for Orcaslicer I've this Start-Gcode
      # Use absolute coordinates 
    G90 
    # Home the printer 
     G28 
     # Reset extruder 
    G92 E0
    BED_MESH_CALIBRATE AREA_START={first_layer_print_min[0]},{first_layer_print_min[1]} AREA_END={first_layer_print_max[0]},{first_layer_print_max[1]}
    # Heat the bed and wait
    M190 S60
    # Move to wait position 
    G1 X0 Y0 Z50 F4000.0  
    # Set and wait for nozzle to reach temperature 
    M109 S210
    # Move Z axis up 
    G1 Z2.0 F3000 
    # Move to start position 
    G1 X10.1 Y20 Z0.28 F5000.0 
    # Draw the first line
    G1 X10.1 Y200.0 Z0.28 F1500.0 E15 
    # Move to the side
    G1 X10.4 Y200.0 Z0.28 F5000.0 
    # Draw the second line 
    G1 X10.4 Y20 Z0.28 F1500.0 E30 
    # Reset extruder 
    G92 E0
