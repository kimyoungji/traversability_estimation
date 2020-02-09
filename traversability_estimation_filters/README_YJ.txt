# Description on the robot_filter_parameters.yaml

1. surface normal filter
radius should be radius>5.0*map_resolution

2. slope filter
    slope = acos(surface_normal_z)
    if slope<critical_value:
        slope = 1.0- slope/critical_value
    else: 
        slope = 0.0

3. step filter
    1) get step_height (within the first_window_radius)

    2) get step (withint the second_window_radius)
        nCells = number of cells (have step_height larger than critical value)
        step = min(stepMax, nCells/(n)critical_cell_number*stepMax)

4. roughness filter
    roughness = std of submap (within estimation_radius)

    if(roughness<critical_value):
        roughness = 1-roughness/critical_value
    else:
        roughness = 0
