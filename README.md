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

(In windows)
1 Download zip folder fusion2urdf from github page
1.2 Copy URDF_Exporter to the Desktop

Open file explorer, in the filepath bar, typ %appdata%/Autodesk/Autodesk Fusion 360/API/Scripts/

(In F360)
Tools>AddIns>Scripts and AddIns
URDF_Exporter will show up.

Asks you to create an empty folder for the export results
a prompt on screen will show a successful result.

In the folder you will find a folder with "f360design_description", this is the ROS package. Which needs to be copied (USB/OneDrive) to your Ubuntu machine.



1
NB: if you want ROS connections, also make a copy of those files into your workspace /src and convert the xacro to a urdf file.
NB2: To use ROS with WeBots, have the robot controller set to "ros" or create your own custom controller. if you chose the standard "ros" controller, look into the provided documentation to find how the services and commands are called. That is also available online as part of the WeBots documentations and tutorials on ROS.
