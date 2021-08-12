# RobotSimulator
Final year BEng Robotics project, this is the documentation.
This project covers 3 aims:

1) Making a physical robot's digital design and putting it in a simulator
2) creating a tutorial on setting up a WeBots simulation from a Fusin360 design
3) documentation for a TAROS paper submission on the topic of comparing CoppeliaSim with WeBots in terms of undergraduate use viability.


A workshop is planned for July 2021, further documentation will be uploaded then.


TLDR of the project:

1) download and install this script for Fusion 360: https://github.com/SpaceMaster85/fusion2urdf
2) use the script; pop the files into your WeBots world folder
3) use the urdf to proto script: https://github.com/cyberbotics/urdf2webots
4) then simply start WeBots and import the proto file.

NB: if you want ROS connections, also make a copy of those files into your workspace /src and convert the xacro to a urdf file.
NB2: To use ROS with WeBots, have the robot controller set to "ros" or create your own custom controller. if you chose the standard "ros" controller, look into the provided documentation to find how the services and commands are called. That is also available online as part of the WeBots documentations and tutorials on ROS.


---- added by Olly in prep for ROC318 / RoboSoc Virtual Humanoids ----

New RoboSoc student simulator setup instructions

1. Laptop Setup

1.1 Install Ubuntu 18.04 "Bionic Beaver" Suggest using a spare USB stick to stick Ubuntu onto an old laptop
https://ubuntu.com/tutorials/create-a-usb-stick-on-windows

1.2 Install terminator
Open a terminal, and run the command "sudo apt-get install terminator". Use ctrl+shift+c & ctrl+shift+v when in a terminal to copy/paste.
Open terminator, right click the icon, add to favourites. Terminator, is a greatly improved version of the bog-standard terminal. All the cool kids use it.

1.3 Install ROS-Melodic 
http://wiki.ros.org/melodic/Installation/Ubuntu
- If you are not familiar with ROS, follow the beginner tutorials 1 - 13 http://wiki.ros.org/ROS/Tutorials#Beginner_Level

2. Webots setup

2.1 Install Webots
https://cyberbotics.com/doc/guide/installation-procedure#installation-on-linux
- Click through a few of the demo applications to see how cool it is.

2.2 Install the Webots ROS package
http://wiki.ros.org/webots_ros

3. Scott simulator setup
3.1 Copy/paste the world folder "scott_world" to the desktop
3.2 Create a folder on the desktop named "scott_sim_ws". This will be the ROS workspace for your project.
3.3 Inside the "scott_sim_ws" folder, create another folder "src".
3.4 Inside the "src" folder, copy/paste the ros package "scott_robot".
3.5 Find the file "testWorld.launch" scott_world>launch>testWorld.launch and edit the line
doc="path to the world", replace the quotes inside with the ABSOLUTE address of the webots world where you have imported the robot.


3. Open a terminal (terminator) navigate to the workspace. 
"cd" to change directory, "ls" to list files/folders within the current directory, "cd .." to go back.
Run the command "catkin_make". This will build the workspace so that ROS recognises it.


LAUNCHING:

Open terminal
step 1: cd Desktop/scott_sim_ws
source devel/setup.bash
roscore

new terminal tab (right click)
source devel/setup.bash
export webots home  >>export WEBOTS_HOME=/usr/local/webots

run the simulation: roslaunch <ros package name> <the launch file - webots.launch>



