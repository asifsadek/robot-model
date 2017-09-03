# robot-model
Creating a robot model for Gazebo, which works with ROS
Install all the relevant ROS and Gazebo packages.

# Instructions
Create new folder and change directory into it

`mkdir xyz && cd xyz`

Make src folder

`mkdir src`

Initialize Catkin workspace

`catkin init`

Perform catkin_make

`catkin_make`

Source the setup.bash file in the newly created devel/ folder

`source devel/setup.bash` 

and/or (mostly and) add this to your `~/.bashrc`, so that the ROS package gets sourced everytime you start your terminal.
To do so:

`echo "source replace_this_with_the_location_of_your_directory/xyz/devel/setup.bash" >> ~/.bashrc`

And source the `~/.bashrc`

`source ~/.bashrc`

Add the folders in this repository to your src folder and catkin_make again. 

To launch the gazebo world

`roslaunch robot_gazebo robot_world.launch`

**Note: ** Running it for the first time might take some time as the gazebo world might get downloaded.
If it runs into some issue, go to the base directory of the project, i.e, xyz and run

`rm -rf build/ devel/

catkin_make

source devel/setup.bash

roslaunch robot_gazebo robot_world.launch`
