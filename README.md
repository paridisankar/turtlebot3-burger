# turtlebot3-burger
I have used ros noetic and turtlebot3 for the project

for more information about the rules

1.Setup gazebo simulation

2.Mapping

3.Navigation

1.setup gazebo simulation For my project i have set up turtlebot3 gazebo simulation Install simulation package
$ cd ~/catkin_ws/src/ 
$ git clone -b noetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git 
$ cd ~/catkin_ws && catkin_make

TurtleBot3 World
$ export TURTLEBOT3_MODEL=Burger
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

2.Mapping
Run slam node
 $ roscore
 $ export TURTLEBOT3_MODEL=Burger 
 $ roslaunch turtlebot3_slam turtlebot3_slam.launch
 Run Teleoperation Node(to move your robot using keybord) 
 $ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch map_update_intrerval save the mape 
 $ rosrun map_server map_saver -f ~/map (f is the folder location)

3.Navigation 
$ roscore 
$ export TURTLEBOT3_MODEL=Burger 
$ roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
for other information you cn costumise you own rviz asper your need 




