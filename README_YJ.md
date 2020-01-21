
$ roslaunch traversability_estimation traversability_estimation.launch

$ roslaunch traversability_estimation visualization.launch

$ rosservice call /traversability_estimation/load_elevation_map "file_path: '/home/youngji/workspace/maps/elevation_map2.bag' 
topic_name: '/elevation_mapping/elevation_map'"

<!--$ rosrun image_transport_tutorial my_publisher /home/youngji/workspace/maps/terrain.png-->

$ rosservice call /traversability_estimation/update_traversability
