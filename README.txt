I.DINCER.N.
ISTANBUL TECHNICAL UNIVERSITY

-------------------------------------------------------------

AUTONOMOUS ROBOT NAVIGATION USING ROS 
Clearpath Husky A200 robot navigation with Gazebo and RViz simulations using different SLAM and Path Planning algorithms. 360 degrees laser scan with two SICK LMS511 LIDARs.

------------------------------------------------------------- 
SIMULATION WORLD LAUNCH

$ roslaunch husky_gazebo husky_koridor3.launch

------------------------------------------------------------- 
RVIZ INTERFACE LAUNCH

$ roslaunch husky_viz view_robot.launch

------------------------------------------------------------- 
MANUAL DRIVE with PS3 JOYSTICK

$ roslaunch husky_control ps3_teleop.launch

-------------------------------------------------------------
AMCL 

Global Planners:
	A*
	Dijkstra
Local Planners:
	DWA
	TEB
	
$ roslaunch husky_navigation amcl_astar_dwa.launch 
---or---
$ roslaunch husky_navigation amcl_astar_teb.launch
---or---
$ roslaunch husky_navigation amcl_dijkstra_dwa.launch 
---or---
$ roslaunch husky_navigation amcl_dijkstra_teb.launch

-------------------------------------------------------------

GMAPPING SLAM with Path Planning Algorithms

Youtube Video: https://www.youtube.com/watch?v=Q_ITD5nnFks&t=51s

Global Planners:
	A*
	Dijkstra
Local Planners:
	DWA
	TEB

$ roslaunch husky_navigation gmapping_astar_dwa.launch
---or---
$ roslaunch husky_navigation gmapping_astar_teb.launch
---or---
$ roslaunch husky_navigation gmapping_dijkstra_dwa.launch
---or---
$ roslaunch husky_navigation gmapping_dijkstra_teb.launch

To save the generated map, you can run the map_saver utility:

    $ rosrun map_server map_saver -f <filename>

-------------------------------------------------------------

HECTOR SLAM with Path Planning Algorithms

Youtube Video: https://www.youtube.com/watch?v=HFuBhpLCG8g&t=29s

Global Planners:
	A*
	Dijkstra
Local Planners:
	DWA
	TEB

$ roslaunch husky_navigation hector_slam_astar_dwa.launch
---or---
$ roslaunch husky_navigation hector_slam_astar_teb.launch
---or---
$ roslaunch husky_navigation hector_slam_dijkstra_dwa.launch
---or---
$ roslaunch husky_navigation hector_slam_dijkstra_teb.launch

To save the generated map, you can run the map_saver utility:

    $ rosrun map_server map_saver -f <filename>

-------------------------------------------------------------

PATH PLANNING without MAP

Global Planners:
	A*
	Dijkstra
Local Planners:
	DWA
	TEB

$ roslaunch husky_navigation move_base_mapless_astar_dwa.launch
---or---
$ roslaunch husky_navigation move_base_mapless_astar_teb.launch
---or---
$ roslaunch husky_navigation move_base_mapless_dijkstra_dwa.launch
---or---
$ roslaunch husky_navigation move_base_mapless_dijkstra_teb.launch

---------------------------------------------------------------------------------------------------


