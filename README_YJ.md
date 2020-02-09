# Line by Line
$ roslaunch traversability_estimation traversability_estimation.launch

$ roslaunch traversability_estimation visualization.launch

$ rosservice call /traversability_estimation/load_elevation_map "file_path: '/home/youngji/workspace/maps/cassie2/elevation_map_full1.bag' 
topic_name: '/elevation_mapping/elevation_map'"

<!--$ rosrun image_transport_tutorial my_publisher /home/youngji/workspace/maps/terrain.png-->

$ rosservice call /traversability_estimation/update_traversability

$ rosservice call /traversability_estimation/save_traversability_map_to_bag "file_path: '/home/youngji/workspace/maps/cassie2/traversability_full1.bag' 
topic_name: 'traversability_estimation/traversability_map'"


#Automatically 
$ roslaunch traversability_estimation traversability_estimation.launch

$ rosservice call /traversability_estimation/load_and_save_traversability_map "file_path: '/home/youngji/workspace/maps/cassie2/'" 
