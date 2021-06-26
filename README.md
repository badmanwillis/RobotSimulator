# RobotSimulator
Final year BEng Robotics project, this is the documentation.
This project covers 3 aims:

1) Making a physical robot's digital design and putting it in a simulator
2) creating a tutorial on setting up a WeBots simulation from a Fusin360 design
3) documentation for a TAROS paper submission on the topic of comparing CoppeliaSim with WeBots in terms of undergraduate use viability.


A workshop is planned for July 2021, further documentation will be uploaded then.


TLDR of the project:

download and install this script for Fusion 360: https://github.com/SpaceMaster85/fusion2urdf
use the script; pop the files into your WeBots world folder
use the urdf to proto script: https://github.com/cyberbotics/urdf2webots
then simply start WeBots and import the proto file.

NB: if you want ROS connections, also make a copy of those files into /src and convert the xacro to a urdf file.
To use ROS with WeBots, have the robot controller set to "ros" or create your own custom controller. if you chose the standard "ros" controller, look into the provided documentation to find how the services and commands are called. That is also available online as part of the WeBots documentations and tutorials on ROS.
