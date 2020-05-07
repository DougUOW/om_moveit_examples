# om_moveit_examples
###### Example code for using MoveIt! with Open Manipulator-X

This package is designed to provide some example code to help getting started using the Open Manipulator-X with ROS and Gazebo. All coding is done in Python.

## System Setup
###### Hardware
Intel NUC, OpenCR development board and Open Manipulator-X with XM430-W350-t motors

###### Software
- Intel Nuc is running Ubuntu 16.04 LTS
- Have installed all ROS packages as stated in Open Manipulator-X eManual
- OpenCR is running usb_to_dxl
- Dynamixel motors setup as per Open Manipulator-X eManual

*Note*  
If using OpenCR, USB port address may need to be changed in joint_trajectory_controller.launch from USB0 to ACM0.  

## Codes
###### execute_trajectory.py
This code will use MoveIt to execute a pre-planned routine. In the attached YouTube video, it can be seen that this code will pick up a cube, then replace the cube.  
###### get_data.py
This code will display various information about the MoveIt setup that is running.  
###### testing_effort.py
Work in progress.  

## YouTube Links
The following links will provide video of the Open Manipulator-X being used in both hardware and simulation using MoveIt!  

###### Open Manipulator-X. ROS. MoveIt! Implementation on physical hardware.  
https://www.youtube.com/watch?v=8yzPcjxFebg  
  
###### Open Manipulator-X. ROS. MoveIt! Gazebo Simulation.  
https://www.youtube.com/watch?v=TV_2RlyWlSc&t=19s  

## Execution 

###### Running on Real Open Manipulator-X
roslaunch open_manipulator_controllers joint_trajectory_controller.launch sim:=false  
rosrun om_moveit_examples execute_trajectory.py  
